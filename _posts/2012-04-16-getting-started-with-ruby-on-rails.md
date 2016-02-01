---
layout: post
title: "Getting started with Ruby on Rails"
date: 2012-04-16 12:00:00
permalink: /entry/getting-started-with-ruby-on-rails
author: Matt Halliday
---

Over the past few months I've been teaching myself Ruby on Rails. I'm very happy with the progress I've made and thought it would be helpful if I shared a bit of my learning process with others.

## My background
I'm a front-end designer, so most of my time is spent writing HTML, CSS and JavaScript. As much as I love doing that, I also wanted to explore the other side of things.

I can write some PHP and understand even more, but it's never really felt natural to me. It always seems that what I'm trying to express in my head makes more sense than the code I write. This left me looking for a different programming language, one that more closely matched how I solved problems in my head.

(Note: I'm not trying to bash PHP here, just stating that it's not for me. Use whatever tools make you happy.)

## So, why Ruby on Rails?
There are many things to love about both Ruby and Rails, but the one thing that stood out to me was the Ruby language itself - it's absolutely *beautiful*.

Ruby doesn't heavily rely on things like curly braces and semicolons, instead line breaks and indentation are used. As a result you end up with groups of code that look like statements written in plain English. Ruby is quite often [compared to poetry](http://37signals.com/svn/posts/3142-on-poetry-programming) because of this.

And since formatting is so important, Ruby code will look virtually the same, even if it's written by different people. This makes it much easier to read if you're working with a team of developers or contributing to open source projects.

Language and syntax aside, there are many other reasons why Ruby on Rails seemed like a good fit for me. Here are just a few:

- Tons of awesome stuff is [built with Rails](http://rubyonrails.org/applications) (Basecamp, Github, Shopify and many others)
- Testing your code is strongly encouraged because it makes your life easier in the long run
- Coding principles like [convention over configuration](http://en.wikipedia.org/wiki/Convention_over_configuration) and [Don't Repeat Yourself](http://en.wikipedia.org/wiki/Don't_repeat_yourself)
- There's a huge [open-source community](https://github.com/languages/Ruby) of friendly, helpful people

## Jump in
I honestly don't think it matters where you start. A lot of people will tell you how to learn, when really, only you will know best. The important thing is that you just get started and stick with it.

I use a lot of different resources, both free and paid, but I had my ["A-ha!" moment](http://en.wikipedia.org/wiki/Aha!_moment) when I did the Rails for Zombies course.

### [Rails for Zombies](http://codeschool.com/courses/rails-for-zombies)
A free online course put out by Code School where you write code directly in the browser. This lets you learn Rails without having to set up a development environment on your machine.

Basically, you watch a video walkthrough and then write code in your browser to reach the next level. Also, be sure to check out Rails For Zombies 2 and also Rails Testing For Zombies.

### [Rails Tutorial](http://railstutorial.org)
A tutorial (recently updated for Rails 3.2) that will walk you through the creation of a simple Twitter-like app.

You'll learn about Rails MVC, testing with RSpec, user authentication, the Asset pipeline and even deploying to Heroku. You can currently read it for free online, or buy the PDF & screencasts.

### [Railscasts](http://railscasts.com)
A great site with new screencasts each week (one free, one pro and one revised). All sorts of topics are covered such as customizing/optimizing Rails, working with Gems and refactoring your code.

Also, if you buy a subscription then you get access to all the pro and revised screencasts.

### [Agile Web Development with Rails](http://pragprog.com/book/rails4/agile-web-development-with-rails)
This is probably the best Rails book out there. It covers tons of useful stuff like testing, AJAX, authentication, sending mail and deploying apps. It's also written by very talented people, including David Heinemeier Hansson, the guy who created Rails.

### [RailsGuides](http://guides.rubyonrails.org/)
This will be your best friend when you're first getting started and can't remember how to do something. I can't tell you how many times I refer to this when I'm working with Rails.

## The path of least resistance
If you take anything away from this article, make sure it's this section. These may seem obvious to some of you, but a list like this would've made my life a lot easier when I was starting out.

### Embrace the command line
It can seem daunting at first, but it's very powerful and faster than browsing your filesystem. I put this off and did things the hard way for a while. It's totally possible, but can be tedious.

### Love thy editor
I prefer something like Textmate (or Sublime Text 2) because it lets me see the entire directory structure which can be helpful when you're starting out. A lot of developers swear by Vim because they're in the command line anyways and it's one less app to switch between. Either way, make sure you love it because you'll be spending 90% of your time using it.

### Have MVC experience
You'll be way ahead of the game if you've worked with other MVC frameworks in the past. If you write procedural code, start with learning the basics of MVC. Simply knowing where all the code lives can be helpful when things go wrong and you need to debug.

### Know some Ruby!
Rails isn't a language, it's a framework built with Ruby. That means you're going to be writing Ruby, so learn it sooner rather than later. It will also give you a better understanding of how Rails works.

## Next steps
One thing I didn't cover here was setting up a Ruby on Rails environment of your own. This looks and sounds harder than it actually is, but it can be intimidating to tackle on your own. I should be publishing an article on that in the next few weeks, so stay tuned and start hacking.
