---
layout: post
title: "What I did next with Octopress"
date: 2013-01-19 22:30
comments: true
categories: [Octopress]
---
## Themes

I saw a website called [Ewal.net](http://www.ewal.net) that I liked the look and feel of and contacted the guy behind it, he said the theme was based on [Slash](https://github.com/tommy351/Octopress-Theme-Slash).

I started by installing Slash.

    cd octopress
    git clone git://github.com/tommy351/Octopress-Theme-Slash.git .themes/slash
    rake install['slash']
    rake generate
    rake deploy
    
<!-- more -->    
    
Didn't really like it, and when I looked at [https://github.com/ervwalter/octopress-ewal](https://github.com/ervwalter/octopress-ewal) I couldn't see **slash** in the `.themes` directory.

Reverted changes.

    rake install['classic']
    rake generate
    rake deploy
    
Maybe adding another theme should be left for another day. However I'm impressed with the ease that the theme could be changed.

## Customisations

My source of inspiration was again [Ewal.net](http://www.ewal.net) and an article about [customisations](http://www.ewal.net/2012/09/08/octopress-customizations/). I decided to try a few.

I removed **blog** from the URL. I like the idea of [FancyBox](!g), but I am not sure of the best way to integrate it to my Markdown workflow.

The next change I made was to add the line

    system "mate \"#{filename}\""
    
to the **new_post** section of the `Rakefile`. This opened up the new post in TextMate.

## Comments

[Octopress][1] supports [Disqus][2] comments. I wanted to enable these on the site. I went to [Disqus][2] and signed up, registered the site [resourcemine][3], and edited the `_config.yml` file to add my `disqus_short_name` and `disqus_show_comment_count`. Note the `disqus_short_name` is the shortname from [Disqus][2].

[1]: http://octopress.org/ "Octopress"
[2]: http://disqus.com/ "DISQUS - Elevating the discussion"
[3]: http://www.resourcemine.net



