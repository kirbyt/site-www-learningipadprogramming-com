---
layout: post
title: 'Using Xcode 4.2 on Snow Leopard'
categories:
  - learn-ipad-book
  - osx
  - xcode

---

A few people have recently mentioned to me that they are still running Snow Leopard (Mac OS X 10.6). The latest version of Xcode requires Lion (Mac OS X 10.7), however, Xcode 4.2 for Snow Leopard is still available for download from the Apple web site.

Learning iPad Programming was written based on Xcode 4.2, so everything covered in the book, with one exception, works with Xcode 4.2 on Snow Leopard. The one exception is the "Allows External Storage" flag in Core Data. This flag is discussed in Chapter 13 on Page 308, and the flag requires Lion. Compile errors are generated if you set this flag while running on Snow Leopard. Not to worry. You can still build the app without setting this flag. The app, after all, is a sample app so for the purpose of learning it is okay to not use this flag when using Xcode 4.2 on Snow Leopard.

To download Xcode 4.2 for Snow Leopard, go to [https://developer.apple.com/downloads/][downloads] and sign in with your Apple Developer ID. In the search box, type "Xcode 4.2". The search results will show Xcode 4.2 for Snow Leopard (see the screenshot below). Use this version of Xcode if you are still running on Snow Leopard.

![Downloads](/images/blog/2012-03-24/Downloads.png)

As an alternative, you can sign into the [iOS Dev Center][iosdevcenter] and scroll down to the Downloads area to find the download link to Xcode 4.2 for Snow Leopard. 

![iOS Dev Center Apple Developer](/images/blog/2012-03-24/iOS-Dev-Center-Apple-Developer.png)

[downloads]: https://developer.apple.com/downloads/ 
[iosdevcenter]: https://developer.apple.com/devcenter/ios/ 