---
layout: post
title: "Getting OEID up and running"
date: 2013-01-19 16:45
comments: true
categories: [Rittman Mead, Endeca, Business Intelligence]
---
### Create the project

Create new Integrator project

![](https://dl.dropbox.com/u/299238/2013-01-18_23-01-04.png)

Create OEID data store

Copy the `workspace.prm` file from the quickstart application. Edit the `workspace.prm` file. Change the parameter `DATA_STORE_NAME`.

<!-- more -->

### Create the data store

Create a new graph called InitDataStore. Copy one component that contains the web service call to create a data store. Just copy the **Create Data Store** component.

![](https://dl.dropbox.com/u/299238/2013-01-18_23-11-43.png)

### Run the graph

Use the run button. Test by pinging the URL [http://localhost:7770/admin/data-store-name?op=ping](http://localhost:7770/admin/data-store-name?op=ping) (Note: 7770 is the default port the Endeca Server runs on).