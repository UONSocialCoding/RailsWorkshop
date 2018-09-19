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

Firstly, Rails and Ruby are a match made in heaven. They're both driven by the same philosophies, and are both very well designed. Unlike many languages Ruby is actually enjoyable to write, and it's easy to learn too. Rails is like Terminator 2: it fully realises the landscape of the original, and builds on top of it in a way that would make Arnie proud.

*Slide*

...

*Slide*

Rails has this notion of convention over configuration. I'm sure you've seen it in the Rails guides already, and maybe even heard me rant about it once or twice. There's good reason for this believe me! Rails teaches you good conventions, and so the skills you learn on a Rails app, will apply to any other web engineering setup. Good conventions means easier maintenance, less hair pulling, and a more enjoyable development experience.

*Slide*

Don't get me wrong, Rails has its flaws. But I'm going to help us navigate through them as best I can.

*slide*

...

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

You may also see this notation from time to time. It's conventional (and strongly encouraged) to use these kinds of methods instead of using double equals.

...

*Slide*

Symbols are a concept you don't often come across in programming languages. The only other time I've encountered symbols is in JavaScript, and they're pretty hidden away there. A symbol is like a meaner, leaner version of a string. Internally, Ruby uses symbols to label things like methods and variables. But we can also use them like enumerators, since they're essentially immutable.





*Slide*

...

*Slide*

Real people will be using your code. And that's a daunting thought. If there's a bug in production, we lose time, money, and potentially even customers.

In case you weren't already shaking in your boots, we have to deal with potential security vulnerabilities as well. If something pops up in production, and believe me it will, we have to drop everything in our lives and release a patch *yesterday*. That's a big responsibility.

It's a terrifying situation but there are steps we can take to protect ourselves and our clients.

*Slide*

I've been thinking about this a lot recently, and I've devised some ways we can protect ourselves.

*Slide*

...

*Slide*

Fortunately for us, Rails has a fantastic testing environment. Whenever you generate a controller, a model, or a mailer, Rails automatically generates corresponding tests.

*Slide*

In case you're curious what tests look like in Rails, here's a real test I wrote that is now in production.

...

*Slide*

By atomic, I mean focus on a single feature. If you want to add two separate features, it's best to have two separate branches and two separate pull requests.

This is super important. If you're branches become bloated, it becomes difficult to merge changes, and a nightmare to review. As Adam and I discovered in the final web engineering assignment.

Also, some of the automated tools stop working once pull requests become too large.

*Slide* 

Rubocop is a static code analysis tool. And it is **brutal**. It analyses your Ruby and tells you 15 thousand things you've done wrong. Rubocop will be both your worst nightmare and your best friend.

*Slide*

Every pull request you make will be scrutinised by continuous integration. It runs tests, checks your code style, reports coverage, and flags potential issues. 

*Slide*

The best part about continuous integration, is that it runs automatically. So you get feedback on your code as soon as you make a pull request.

*Slide*

...

*Slide*

I can't stress this enough. The only time we will ever push to production is when we are positive we have a stable build. To aid in our ventures, we're going to also setup a staging environment, accessible only to the developers.

The staging environment will be identical to our production environment as far as technology goes. The only difference, will be that staging is kept on the bleeding edge.

Believe me, it will bleed.

*Slide*

I'm going to randomly assign two of you to every pull request. If you're assigned to a pull request, it's your job to scour through the proposed changes and provide some feedback.

GitHub provides you with some great tools for making suggestions on a line-by-line basis, or providing general feedback.

No pull request will ever be merged if it hasn't been reviewed by people.

*Slide*

...

*Slide*