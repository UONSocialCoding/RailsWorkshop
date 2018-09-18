Thanks for coming.

*Slide*

The single most important take away of this workshop, is that bottom point 
there. We all need to understand and appreciate the production work flow.

*Slide*

First, I should mention that we don't explicitly *need* to use a web framework. We could easily build a web server from scratch in C++, Java, or any other language for that matter. But we only have a year, and ideally I'd like to enjoy that year. 

So there are tonnes of web frameworks out there: Django, Flask, Tomcat, Spring, Struts etc. etc. And I've played around with a bunch off them, and none compare to Rails.

So why is this?

*Slide*

It's difficult to point to any single reason, but I do have I few theories.

Firstly, Rails and Ruby are a match made in heaven. They're both driven by the same philosophies, and are both very well designed. Ruby is actually enjoyable to write, and Rails is like the Terminator 2 sequel. 

*Slide*

Rails fully realises the landscape of the original (that's Ruby if it's not obvious), and builds on top of it in a way that would make Arnold proud.

*Slide*

Rails has this notion of convention over configuration. I'm sure you've seen it in the Rails guides already, and maybe even heard me rant about it once or twice. There's good reason for this believe me! Rails teaches you good conventions, and so the skills you learn on a Rails app, will apply to any other web engineering setup. Good conventions means easier maintenance, less hair pulling, and a more enjoyable development experience.

...

*Slide*

*Slide*

Here we can see two separate ways to create an array of strings. They're identical. 


...


Notice that in the second array I'm using single quotes. 

*Slide*

The convention in Ruby is to use single quotes for strings unless they have some kind of interpolation or formatting inside them.

...

*Slide*

The important thing here, is to notice that calling `downcase` on a string only returns the result. It does not modify the string itself. 

*Slide*

But when we add an exclamation mark to the end of the method, suddenly our result changes. In Ruby, when a method returns a modification of our original object, it's conventional to make two versions. One with an exclamation mark and one without.

This is something you might want to keep in mind when reading and writing Ruby.

*Swap repeatedly back and forth between previous slides.*