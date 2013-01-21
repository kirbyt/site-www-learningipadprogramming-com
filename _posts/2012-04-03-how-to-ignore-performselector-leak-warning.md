---
layout: post
title: 'How To Ignore performSelector Leak Warning'
categories:
  - ios
  - learn-ipad-book
  - photowheel

---

In Listing 16.22 from the Learning iPad Programming book, I show how to invoke a method using `-performSelector:` where the selector is determined at runtime from a set of names stored in an NSArray. The implementation in Listing 16.22 could have been done a number of different ways, but I chose this approach to show how to set and perform a selector at runtime. However, the code produces a compiler warning message when ARC is used. 

Because ARC is used and the selector is determined at run, the compiler generates a "possible memory leak" warning message. This warning is legitimate given that the selector is unknown at compile time and ARC is being used to manage memory.

At the time the code in Listing 16.22 was written, there was no way to ignore this warning message. That can be a good thing since explicitly ignoring a warning message from the compiler can be a bad thing. 99.9% of the time you want to fix or refactor your code so the warning message goes away. However, there are times when you know more than the compiler does, and the code in Listing 16.22 is one of those rare times. 

In this particular case, each selector that can potentially be called will not cause a memory leak because each one returns a void. The compiler doesn't know this, but you (as the programmer) know this to be true. So this warning message can safely be ignored. But how do you tell the compiler to ignore the `-performSelector:` possible memory leak warning so you don't have to see the warning message each time you compile the project?

You can use tell clang to ignore the -performSelector leak warning by wrapping the `-performSelector:` call with a set of `#pragma` statements that temporarily ignore the warning for the code included in the block. Here is an example:

```
#pragma clang diagnostic push
#pragma clang diagnostic ignored "-Warc-performSelector-leaks"
   [self performSelector:selector];
#pragma clang diagnostic pop
```

So the code causing the warning message in Listing 16.22 for the PhotoWheel app now looks like this:

{% codeblock lang:objc %}
- (void)actionSheet:(UIActionSheet *)actionSheet clickedButtonAtIndex:(NSInteger)buttonIndex
{
   // Do nothing if the user taps outside the action 
   // sheet (thus closing the popover containing the
   // action sheet).
   if (buttonIndex < 0) {
      return;
   }
   
   NSMutableArray *names = [[NSMutableArray alloc] init];
   
   if ([actionSheet tag] == 0) {
      [names addObject:@"confirmDeletePhotoAlbum"];
      
   } else {
      BOOL hasCamera = [UIImagePickerController isSourceTypeAvailable:UIImagePickerControllerSourceTypeCamera];
      if (hasCamera) [names addObject:@"presentCamera"];
      [names addObject:@"presentPhotoLibrary"];
   }
   
   SEL selector = NSSelectorFromString([names objectAtIndex:buttonIndex]);
#pragma clang diagnostic push
#pragma clang diagnostic ignored "-Warc-performSelector-leaks"
   [self performSelector:selector];
#pragma clang diagnostic pop
}
{% endcodeblock %}  
