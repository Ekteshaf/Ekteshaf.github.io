---
layout: post
title: Jekyll Has Been Unleased
description: "Getting this site."
category: articles
tags: [jekyll, so simple, node.js, static site generators, ubuntu]

comments: true  
---

Web dev is one of the cooler parts of programming, but was also frustrating for me to get through (the manual work associated with html and css *shivers*). Despite that I decided I might as well try to make a personal website just for the fun of it.

###Static Site Generators???

Not long after I heard about these nifty 'static site generators' which took out all the manual html work. Particularly I was exposed to Jekyll as I was learning through github pages which mentioned it. Jekyll specifically is a ruby gem, which lets you create a blog specific website where posts can be written in markdown (which will be converted to html...this was reason enough to try it). At this point I had no experience with ruby or node.js, but might as well try...


###Getting Jekyll:

I was primarily running Ubuntu at this point so that made the process a lot more fun since I could just abuse the terminal. Easy enough get ruby, then follow the instructions on the website spiced with the power of sudo.

~~~~
~$ sudo apt-get install ruby1.9.1-dev
~$ sudo gem install jekyll
~~~~
There ended up being an error here due to some docs being missing and upon further investigation it was the docs.

~~~~
~$ sudo gem install rdoc
~$ sudo gem install jekyll
~~~~

###Using This:

Never used static site generators before so I had to spend some time going through the [docs][jekylldocs]. The important concept came from the directory structure (all content from the jekyll docs):

~~~~
.
├── _config.yml
├── _drafts
|   ├── begin-with-the-crazy-ideas.textile
|   └── on-simplicity-in-technology.markdown
├── _includes
|   ├── footer.html
|   └── header.html
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.textile
|   └── 2009-04-26-barcamp-boston-4-roundup.textile
├── _data
|   └── members.yml
├── _site
└── index.html 
~~~~
and also the commands to actually create webpages:

~~~~
~$ jekyll new my-awesome-site
~~~~
 
 And running them locally:
 
~~~~
~ $ cd my-awesome-site
~/my-awesome-site $ jekyll build
~/my-awesome-site $ jekyll serve
~~~~

###Customizing:

At this point the backbone of this site was made and all that was needed were some content and design. I didn't find the default designs too good so I decided to use the open source [So Simple Theme][simplegit] since it looked so stellar and rocked the minimilist design which is mainstream nowadays.

**Shout out to** [Victor][domain] for informing me about gihub pages and enlightening me on the magic of static site generator.

[simplegit]:https://github.com/mmistakes/so-simple-theme
[jekylldocs]:http://jekyllrb.com/docs/home/
[domain]:http://victorszeto.com/

