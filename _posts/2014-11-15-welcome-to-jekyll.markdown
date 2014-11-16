---
layout: post
title:  "On Jekyll and Blogging"
date:   2014-11-15 22:33:01
permalink: /posts/welcome-to-jekyll
categories: jekyll
---
This weekend I'm lucky enough to be attending my second Railscamp. Rather than focusing on building some awesome project and learning loads of Ruby or other languages along the way. This time I decided my focus would be on more of a soft skill I feel I need to practice: Just ship it! So my goal is simple. To complete something.

![Woodman Point]({{ site.base_url }}/images/woodmanpoint.jpeg)

## The Hunt for the Best Blogging Tool
After a quick statistically insignificant survey of the people around me there were three popular tools for us Ruby developers to use to setup a blog. Here's my summary:
Ruby on Rails. Too much overkill for a blog. I've had plenty of practice so I was keen to give something else a go.
Middleman. I've been meaning to check out middleman for quite some time as a blogging platform. It seems really simple to setup with either Heroku or GitHub pages. 
Jekyll. Super easy integration with GitHub pages was a win for me. I can build the site and run it on my local server. But pushing to a simple GitHub branch via the command line is enough to get it live on the site. Plus it's ruby and I can use markdown. So this is the one.

## Setting up a Blog with Jekyll is Super Simple!
There are quite a few resources around for setting up a blog with Jekyll along with a number of tempalates you can use for design. I played around with a few of them before trashing them all and starting with the most basic setup. This is what's needed if I want to host on Github pages and also be able to run my server to check out pages locally.

Install Jekyll, which is a ruby gem.   
`$ gem install jekyll`

If you already have Jekyll installed or want to check it installed successfully.   
`$ jekyll --v`

Starting from the directory you want your blog to be located.   
`$ jekyll new amanda_blog`

Switch into your new blog directory that was created.   
`$ cd amanda_blog`

Open it up in your favourite editor (I'm currently using Sublime Text).   
`$ subl .`

Edit your _config.yml file to add the following details:   
{% highlight yaml linenos %}
title: AmandaNeumann.com
email: amandaneumann@me.com
description: Random thoughts from an educationalist turned apprentice code ninja.
baseurl: /amanda_blog # the subpath of your site, e.g. /blog/
url: "http://amanda08.github.io" # the base hostname & protocol for your site
twitter_username: amandamelb
github_username:  amanda08

# Build settings
markdown: kramdown

{% endhighlight %}

Run your server to load Jekyll on your local machine.   
`$ jekyll serve --baseurl '' --watch`   
Note the --baseurl flag '' ensures it overrides the baseurl setup in your config so that it runs from localhost on your local machine. The --watch flag means Jekyll will automatically update your build each time you make a change to your files.


Now the moment of truth... open your favourite browser and head to `localhost:4000`

If all's gone well you should see your awesome new blog! Jekyll gives you a nice default post with some helpful tips to get you started creating your first post.

## Pushing to GitHub Pages


