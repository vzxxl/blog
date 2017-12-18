---
layout: post
title: Simple blog on Jekyll with free hosting on GitHub
date: 2017-12-18 12:58:20 +0300
description: How to build a blog in no time and zero expenses. # Add post description (optional)
img: jekyll.png # Add image post (optional)
tags: [blog, jekyll, github]
---
Have you ever thought about the possibility of making a blog quickly and with no pyments at all, even for hosting. Well, nowadays with all these new services we can do so much more. And in this post Im going to tell you about this possibility with GitHub and Jekyll. 
If you work in IT you probably know about Git and GitHub where you can store your code and track all the changes you have implemented to it. But not everyone knows that GitHub also allows you to host your site and veiw it like a normal one. It's called <a href="https://pages.github.com/">GitHub Pages.</a>

![GitHub Pages]({{site.baseurl}}/assets/img/github-pages.jpg)

Seems like now we have a solution. But there is one problem: you can't use a database on GitHub Pages. But here's why I love IT community and "problem-solving" type of thinking - sooner or later there will be a way around. This time GitHub programmers solved this problem themselvs creating Jekyll - a Ruby gem that can make a blog out of static html elements. And don't be scared by Ruby language, you don't need to know it to work with Jekyll. Its so simple that even a no-it guy could figure it out. You can find more information about <a href="https://jekyllrb.com/">Jekyll</a> on their official website.  

![Jekyll Website]({{site.baseurl}}/assets/img/jekyll-official.jpg)

## Lets make it by steps
First of all you need to install Ruby environment. If you don't know weather it is already in your system or not, try to check the version by typing this command in the terminal:
<p class="code-field">ruby -version</p>
If there's no info, then install it by this command (For Linux):
<p class="code-field">sudo apt-get install ruby-full</p>
There are other ways to install ruby for different systems. Check <a href="https://www.ruby-lang.org/en/documentation/installation/">this site </a>for more info

Second step is to install jekyll. It is a so-called ruby gem (like a module in Node JS). You can do it by this command:
<p class="code-field">gem install jekyll bundler</p>
<p class="code-field">jekyll new name-of-you-project</p>
<p class="code-field">cd name-of-you-project</p>

Now you have Jekyll project ready. All main configurations are in <strong>_config.yml</strong> file. If you want to see how does the default theme look you can run a local server. Jekyll aready has all the settings for that. Simply type this command in the terminal

<p class="code-field">jekyll serve</p>

Now you can open your site here <strong>http://127.0.0.1:4000/name-of-your-project/</strong>. You can also find the project name in <strong>_config.yml</strong>. If you're too lazy to deal with front-end building process from scratch, you have a wonderful option to download a ready-to-use theme on <a href="http://jekyllthemes.org/">JekyllThemes.org.</a> Here you can choose from dozens of designs and change the parts that you don't like later. 

After figuring out the common structure of jekyll theme folder you are ready to put it to the GItHub. I suppose you already have an account there. So, first of all, you need to make a local adding to the GIT system:

<p class="code-field">git add .</p>//adds all the files to GIT
<p class="code-field">git commit -m "your comment for this commit"</p>//fixates the current condition of your code

Now make a new repository on GitHub and copy a link to it

![GitHub instruction]({{site.baseurl}}/assets/img/github-instruction.jpg)

Now you can send your code and files to GitHub:

<p class="code-field">git remote add origin your-link-to-the-repository</p>
<p class="code-field">git remote -v</p>
<p class="code-field">git push origin master</p>

We are almost there. We have our code and files on GitHub in master branch. But actually we need it to be in gh-pages branch. So few other commands needed:

<p class="code-field">git branch gh-pages</p>
<p class="code-field">git push origin gh-pages</p>

So that's it. You have your blog hosted on GitHub. Be ready to wait for some time since it takes a while to update the information for GitHub. Some people say it can take few hours. In my case it was just few minutes. 
You can find your site on <strong>your-github-nickname.github.io/name-of-your-repository</strong>

Enjoy blogging!