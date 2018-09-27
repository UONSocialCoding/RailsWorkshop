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

Firstly, Rails and Ruby are a match made in heaven. They're both driven by the same philosophies, and are both very well designed. 

Ruby is a enjoyable to write, and it's easy to learn too. Rails is like the Terminator sequel: it fully realises the landscape of the original, and builds on top of it in a way that would make Arnie proud.

*Slide*

...

*Slide*

Rails has this notion of convention over configuration. I'm sure you've seen it in the Rails guides already, and maybe even heard me rant about it once or twice. There's good reason for this believe me!

Rails teaches you good conventions, and so the skills you learn on a Rails app, will apply to any other web engineering setup. Good conventions means easier maintenance, less hair pulling, and a more enjoyable development experience all round.

*Slide*

Both Ruby and Rails are known for their great communities.

*Slide*

They each have active repos on GitHub, with thousands of contributors, and update cycles planned well into the future.

...

*Slide*

Active communities means constant updates, and new features to play with.

...

*Slide*

They also have fantastic documentation, covering just about every topic you can imagine. If you're looking to learn more about Rails then the official guides are the best place to start.

*Slide*

Don't get me wrong, Rails has its flaws. But I'm going to help us navigate through them as best I can.

*Slide*

...

*slide*

...

*Slide*

It's conventional in Ruby to use single quotes for strings, unless they have some kind of interpolation or formatting inside them.

...

If you're coming from other languages, this is probably pretty unusual.

*Slide*

This is how you create an array in Ruby.

*Slide*

And here's another way. There are often multiple ways of achieving things, which can be daunting for newcomers to the language.

...

*Slide*

For example, here's one way create a hash. If you're not familiar, hashes are just like dictionaries in Python, or HashMaps in Java: they store key to value relationships.

Here we can see the symbol *apple*, mapping to the string '*fruit*'.

...

*Slide*

A few years ago a newer, slimmer hash syntax was introduced. Both syntaxes are considered valid ways to define a hash, but it's generally recommended to use the newer syntax because it's easier to read, and is more consistent with languages like Python, JavaScript, and JSON.

...

*Slide*

And here's a third, more convoluted way to create hashes with two arrays.

...

*Slide*

Note that all three of these techniques result in identical output. With number 2 being far and away the most common in modern Ruby.

...

*Slide*

You may have come across blocks already, but did you know there are multiple ways to write blocks as well? Here we can see a block denoted by the keywords `do` and `end`.

...

We can simplify this down a bit more.

*Slide*

This is an inline block. It's particularly useful if you only want to execute a single statement. We trade our `do` and `end` keywords for curly braces, and move the whole expression inline.

...

But believe it or not we can take this one step further.

*Slide*

Since the block only calls a single method on each element, we can use a method reference. Obviously this cuts down massively on code size, and in my opinion improves readability as well.

...

There's one last thing we can do here though....

*Slide*

...

*Slide*

...

*Slide*

There are so many more Rubyisms that we could discuss, but I don't want to overload you guys, and I'm sure you'll pick them up along the way. If you do want to know more, you can always Google one of these topics or ask me about it at some point.

...

*Slide*

...

*Slide*

...

*Slide*

Answer: There is no increment operator in Ruby. There is no decrement operator either. You have to use plus equals and minus equals instead.

*Slide*

...

*Slide*

Answer: Else if is written as elsif in Ruby.

*Slide*

...

*Slide*

Answer: If you put a range inside square brackets, your code will be interpreted as a range inside an array. The solution is to swap the brackets for parenthesis. Note that we do actually need parenthesis here, because a single dot has higher operator precedence than a double dot.


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

This is super important. If you're branches become bloated, it becomes difficult to merge changes, and a nightmare to review. Also, some of the automated tools stop working once pull requests become too large.

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

I'm going to assign at least one person to every pull request. If you're assigned to a pull request, it's your job to scour through the proposed changes and provide some feedback.

GitHub provides you with some great tools for making suggestions on a line-by-line basis, or providing general feedback.

No pull request will ever be merged if it hasn't been reviewed by at least one human.

*Slide*

...

*Slide*