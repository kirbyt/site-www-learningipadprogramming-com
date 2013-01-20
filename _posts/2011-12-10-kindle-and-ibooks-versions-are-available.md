---
layout: post
title: 'Kindle and iBooks Versions are Available'
categories:
  - books
  - learn-ipad-book

---

The <a href="http://amzn.to/ipadprogbook-kindle">Kindle</a> and iBooks Store versions of Learning iPad Programming are now available for purchase and download. This is exciting but at the same time a little disappointing for me. Why? I'm not happy with some of the formatting errors found in the digital version of the book. The two most obvious formatting errors are shortcut keys and source code listings.

Something strange happened with the shortcut keys. Tom and I were asked to use the Command symbol (⌘) instead of typing the word Command. For example, Option-⌘-4 instead of Command-Option-4 (which was my style before writing this book). Two things happened with the Command symbol. First, in cases were it is displayed in the epub version of the book, the symbol floats up high. In the Kindle version, the symbol appears on its own line. But worse than this is when the letter "c" is displayed in place of the Command symbol.

Chapter 2 is the worse hit chapter with regard to the "c" problem, as I know call it. So instead of seeing Option-⌘-4 you see Option-c-4. These two keystroke sequences are completely different, and trust me, Tom and I did not type in Option-c-4 in the manuscript. We used the Command symbol, but unfortunately something strange happened when the digital versions of the book were made.

The other problem is with source code listings. The source code listings were formatted for print, not for the digital version of the book. I use the line wrapping option in Xcode to dynamically format my source code based on the size of the Workspace window. When I copied the code into the manuscript, I again let line wrapping do its thing. But during the copy editor phase, we were asked to reformat the code listings to 80 columns per line. We did this and the code listings should look good in the print version of the book. However, the 80 column format in the ebook version doesn't work. Lines are wrapped at odd places making the source code listings more difficult to read. I believe this would not have been a problem if we left the lines of code as is and let line wrapping do its normal thing.

So I'm exciting that the book is now available (at least in digital format), but I'm also not happy about these two formatting issues. 

To those of you who have (or will) buy a digital copy of the book, I apologize for the formatting issues with shortcut keys and source code listings. I have made the publisher aware of the issues, and I can only hope that a "fix" can be made. (This is my first book, and my first book with this publisher, so I'm not sure what can and cannot be done with regard to fixing the formatting problems.)

<strong>Update:</strong> Tom pointed out to me that the source code format looks better if you reduce the font size in your ebook reader. So give that a try if you are having trouble reading through the source code listings.

<strong>Update:</strong> See <a href="http://learnipadprogramming.com/2011/12/16/kindle-and-ibooks-stores-versions-will-be-available-soon/">here</a> for the latest update.
