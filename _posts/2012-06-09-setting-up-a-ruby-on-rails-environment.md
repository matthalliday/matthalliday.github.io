---
layout: post
title: "Setting up a Ruby on Rails environment"
date: 2012-06-09 12:00:00
permalink: /entry/setting-up-a-ruby-on-rails-environment
author: Matt Halliday
---

Ruby on Rails is a great framework with lots to offer, but to those unfamiliar with either Ruby or Rails, it can be a bit intimidating to get a development environment set up.

Note: I'll only be covering installation for Mac OS X (specifically Lion) because that's what I'm using. Windows users should have a look at [RailsInstaller](http://railsinstaller.org/) and Linux users probably don't need help anyways.

## Custom FTW
There are lots of ways to set up a Rails environment, but I'm only going to cover my preferred configuration, which is using [rbenv](https://github.com/sstephenson/rbenv) and [ruby-build](https://github.com/sstephenson/ruby-build).

A few reasons why we're not going to bother with the default Mac OS X version of Ruby:

- it's already out of date
- it doesn't support multiple versions
- it can easily break after OS upgrades

We're also not going to bother with RVM, but I won't go into the reasons why. If you're curious, just read the rbenv/rvm comparison on the rbenv Github page. (Nothing against RVM, I just prefer rbenv/ruby-build)

## rbenv: Simple Ruby version management
That title doesn't lie - installing [rbenv](https://github.com/sstephenson/rbenv) is pretty simple, but you will need to have Git on your system. If you don't have it yet, you can download and install the Mac package [from the official website](http://git-scm.com/download/mac).

First things first, open up Terminal.app and type the following commands (without the dollar sign - that's used to represent your shell prompt):

	$ cd
	$ git clone git://github.com/sstephenson/rbenv.git .rbenv

If you're unfamiliar with shell commands, all we did was change into our home directory (/Users/yourusername) and cloned a Git repository into a new directory called .rbenv (in OS X any files/folders that begin with a period are hidden by default).

Now in Terminal, type the following:

	$ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
	$ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
	$ exec $SHELL

The commands above should have added a few lines of code to your bash profile (a hidden file located in your home directory). These commands pretty much tell your shell what to do when you type an rbenv command. The last command will restart your shell and let you start using the rbenv command. (If the last command doesn't work, try relaunching Terminal and that should do it.)

Next, enter the following command into Terminal and you should see a help screen with the version of rbenv and all the possible commands.

	$ rbenv

If you don't get an error that means you've done everything correctly - congrats! Now we have rbenv set up, but we still need to install a few more things.

## Enter ruby-build
If you thought installing rbenv was easy, then you'll love [ruby-build](https://github.com/sstephenson/ruby-build), which by the way, are both of which are made by the super awesome [Sam Stephenson of 37signals](http://sstephenson.us/).

We're going to be installing ruby-build as a plugin for rbenv, so you'll need to run the following commands into your Terminal:

	$ mkdir -p ~/.rbenv/plugins
	$ cd ~/.rbenv/plugins
	$ git clone git://github.com/sstephenson/ruby-build.git

The above commands created a subdirectory called plugins in /Users/yourusername/.rbenv, changed into that newly created directory and cloned the Git repo containing ruby-build. You can check ~/.rbenv/plugins to check and see if there's a ruby-build directory there. If there is, it's successfully installed.

Now that we have both rbenv and ruby-build set up and properly working, all we have to do is install the [latest stable version of Ruby](http://www.ruby-lang.org/en/downloads/) and set it as the default version.

In order for this step to work, you'll need to have Xcode installed on your system. You can grab it for free from the Mac App Store if you need to. Once it's installed, run the following commands. (The first command may take a while because it needs to download and compile the Ruby source code.)

	$ rbenv install 1.9.3-p194
	$ rbenv rehash
	$ rbenv global 1.9.3-p194

We're almost done - just a few more steps and you can start using Rails.

### Multiple versions of Ruby
It's worth noting that the above commands will also allow you to install any other versions of Ruby (old or new), simply by changing the build number.

For example, if you needed to support an older Rails app that requires Ruby 1.8, you would type:

	$ rbenv install 1.8.7-p358
	$ rbenv rehash
	$ cd ~/legacy-rails-app/
	$ rbenv local 1.8.7-p358

Then you could have the latest Ruby version set as your system default, but override it on a per project basis using the rbenv local command.

## RubyGems and Rails
Since we'll be installing Rails from the RubyGems library, we want to make sure that we have the latest version. RubyGems should already be installed by default, so all we'll have to do is make sure it's up to date.

	$ gem update --system

Once that's finished updating, we'll need to install the Rails gem.

	$ gem install rails

Rails and RubyGems are now installed and up-to-date.

## Finishing up
Our shiny new Ruby on Rails development environment should now be set up, properly configured and ready to start using.

By choosing the rbenv/ruby-build configuration, we've made it pretty easy for ourselves to stay up-to-date with the latest version of Ruby. We also now have the ability to support legacy Rails apps that may require older versions of Ruby (like 1.8).

If you're wondering what to do next, you may want to read my previous article on [Getting started with Ruby on Rails](http://matthalliday.ca/weblog/entry/getting-started-with-ruby-on-rails).

Also, if you've run into any into problems during the installation process, I'll try my best to answer any questions you may have [on Twitter](http://twitter.com/matthalliday).