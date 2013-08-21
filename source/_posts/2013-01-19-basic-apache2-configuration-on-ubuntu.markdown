---
layout: post
title: "Basic Apache2 configuration on Ubuntu"
date: 2013-01-19 15:53
comments: true
categories: [Octopress, Ubuntu]
---
## Useful links

- [https://help.ubuntu.com/10.04/serverguide/httpd.html](https://help.ubuntu.com/10.04/serverguide/httpd.html)
- [https://help.ubuntu.com/community/ApacheMySQLPHP](https://help.ubuntu.com/community/ApacheMySQLPHP)

## Where is index.html

The default webroot directory is `/var/www/index.html`.

## Setting up Octopress as a site

From: [https://help.ubuntu.com/community/ApacheMySQLPHP](https://help.ubuntu.com/community/ApacheMySQLPHP)

Make a directory.

    mkdir /home/jonmead/octopress/
    
Copy over the default config files.

    sudo cp /etc/apache2/sites-available/default /etc/apache2/sites-available/octopress
    sudo vim /etc/apache2/sites-available/octopress

<!-- more -->

Change the DocumentRoot to point to the new location. For example, `/home/jonmead/octopress/`.

Change the Directory directive, replace `<Directory /var/www/>` to `<Directory /home/jonmead/octopress/>`.

You can also set separate logs for each site. To do this, change the ErrorLog and CustomLog directives. This is optional, but handy if you have many sites

Now, we must deactivate the old site, and activate our new one. Ubuntu provides two small utilities that take care of this: a2ensite (apache2enable site) and a2dissite (apache2disable site).

    sudo a2dissite default && sudo a2ensite octopress

Finally, we restart Apache2:

    sudo /etc/init.d/apache2 restart

If you have not created `/home/jonmead/octopress/`, you will receive an warning message. To test the new site, create a file in `/home/user/public_html/`:

    echo '<b>Hello! It is working!</b>' > /home/jonmead/octopress/index.html

Finally, browse to [http://localhost/](http://localhost/)