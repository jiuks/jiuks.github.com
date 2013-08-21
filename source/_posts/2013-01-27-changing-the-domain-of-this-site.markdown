---
layout: post
title: "Changing the Domain of this Site"
date: 2013-01-27 10:54
comments: true
categories: [Octopress] 
---

## ResourceMine.net

I originally set this site up as an experiment, however I have been impressed with [Octopress][1] and want to use the site as a place to dump my thoughts. resourcemine.net was a domain that I had registered, so I configured the DNS for this domain.

Over the weekend I registered [jonmead.me][7], [jonmead.com][8] and [jonmead.co.uk][9] and I am going to use jonmead.me for this site.

After setting up the DNS for the jonmead.* URLs, these are the steps I took.

<!-- more -->

## Server

The server is running in my basement on [ProxMox][2], its a Ubuntu 12.04  container. By default this had Apache2 installed. I covered [Basic Apache2 Configuration on Ubuntu](/2013/01/19/basic-apache2-configuration-on-ubuntu/) earlier in the month.

There were no changes required to the server, nor my internal network or router.

## Client Setup

I decided to use my MBP 15" retina as the clint I already had [Git][3] and [Ruby 1.9.3][4] installed, so that was easy, and then followed the [Octopress Setup](http://octopress.org/docs/setup/) documentation and chose to [rsync][5] to the above server.

The only configuration changes I made were in `_config.yaml`, as below:

    # ----------------------- #
    #      Main Configs       #
    # ----------------------- #
    
    url: http://jonmead.me
    title: Jon Mead
    subtitle: Men do not quit playing because they grow old; they grow old because they quit playing
    author: Jon Mead
    simple_search: http://google.com/search
    description:
    

## Site Search and Google

As [Octopress][1] is a static blogging framework, its search is done by Google's `site:jonmead.me` directive.

I originally set this site up to capture my thoughts, so hadn't considered Search Engine Opimization (SEO) would be something that I needed to think of, however I wanted to make sure Google was aware of the site so the search would work.

I had configured  [Google Analytics][6] for resourcemine.net, so I needed to repeat the process for jonmead.me.

### Google Analytics

I logged in to http://analytics.google.com, went to the Administer tab and added a new **Web Property**.

![](https://dl.dropbox.com/u/299238/2013-01-27_10-30-46.png)

This gave me a **Tracking ID**, which I could then add to `my _config.yml`. The **Tracking ID** is now added to each page.

The way to access the site is now [http://www.jonmead.me][7]


[1]: http://octopress.org/ "Octopress"
[2]: http://www.proxmox.com/ "Proxmox - Start page"
[3]: http://git-scm.com/ "Git"
[4]: http://www.ruby-lang.org/en/news/2012/11/09/ruby-1-9-3-p327-is-released/ "Ruby 1.9.3-p327 is released"
[5]: http://octopress.org/docs/deploying/rsync/ "Deploying with rsync - Octopress"
[6]: http://www.google.com/analytics/ "Google Analytics Official Website - Web Analytics &amp; Reporting ..."
[7]: http://www.jonmead.me "Jon Mead"
[8]: http://www.jonmead.com "Jon Mead"
[9]: http://www.jonmead.co.uk "Jon Mead"