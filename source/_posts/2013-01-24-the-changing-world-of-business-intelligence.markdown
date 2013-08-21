---
layout: post
title: "The Changing World of Business Intelligence"
date: 2013-01-24 22:12
comments: true
categories: [Business Intelligence, Big Data, Rittman Mead]
---

I have spent the first half of this week in an internal [Rittman Mead](http://www.rittmanmead.com) sales workshop, during which there have been a lot of discussions about the past and future of Business Intelligence, or [Business Analytics](http://www.oracle.com/us/solutions/business-analytics/overview/ "Oracle Business Analytics - Overview | Solutions | Oracle") as [Oracle](http://www.oracle.com) are now calling it.

One thing that struck me was the change in Business Intelligence compared to when I started working in the industry.

<!-- more -->

There used to be a fairly straight forward graphic that was used to explain Business Intelligence.

![](https://dl.dropbox.com/u/299238/2013-01-23_22-31-32.png)

The bottom of the pyramid was the data in the organisation, there was then a transformation layer that turned it into information, it was then consumed by end users as knowledge which could be used in their decision making process.

I feel this has now been replaced by the following graphic.

![](https://dl.dropbox.com/u/299238/2013-01-23_22-33-58.png)

This model still starts with data, however the source, volume, variety and velocity (deliberately borrowed from standard [Big Data](http://en.wikipedia.org/wiki/Big_Data "Big Data") definitions) of this data has increased. The organisation now looks at more internal sources of data, plus external sources of data as well, such as social media and third party market research.

The biggest change is the transformation layer. Depending on the source of data and the questions that are being asked of the organisation there are now two differ approaches: schema on write and schema on read.

### Schema on Write

This is the traditional approach for Business Intelligence. A model, often dimensional, is built as part of the design process. This model is an abstraction of the complexity of the underlying systems, put in business terms. The purpose of the model is to allow the business users to interrogate the date in a way they understand.

The model is instantiated through physical database tables and the date is loaded through an ETL (extract, transform and load) process that takes data from one or more source systems and transforms it to fit the model, then loads it into the model.

The key thing is that the model is determined before the data is finally written and the users are very much guided or driven by the model in how they query the data and what results they can get from the system. The designer must anticipate the queries and requests in advance of the user asking the questions.

### Schema on Read

Schema on read implies works on a different principle and is more common in the [Big Data](http://en.wikipedia.org/wiki/Big_Data "Big Data") world. The data is not transformed in any way when it is stored, the data store acts as a big bucket.

The modelling of the data only occurs when the data is read. Map/Reduce is the clearest example, the mapping is the understanding of the data structure. [Hadoop](http://hadoop.apache.org/ "Welcome to Apache™ Hadoop®!") is a large distributed file system, which is very good at storing large volumes of data, this is potential. It is only the mapping of this data that provides value, this is done when the data is read, not written.

### New World Order

So whereas Business Intelligence used to always be driven by the model, the [ETL][1] process to populate the model and the reporting tool to query the model, there is now an approach where the data is collected its raw form, and advanced statistical or analytical tools are used to interrogate the data. An example of one such tool is [R][2].

The driver for which approach to use is often driven by what the user wants to find out. If the question is clearly formed and the sources of data that are required to answer it well understood, for example how many units of a product have we sold, then the traditional schema on write approach is best.

If the question is more open, for example what is causing our sales of a product to drop, why are customers churning or even [unknown unknowns](http://en.wikipedia.org/wiki/There_are_known_knowns "There are known knowns - Wikipedia, the free encyclopedia"), then the schema on read is most appropriate.

### Decisions, Decisions, Decisions

Whichever approach is taken the end result is that the user, or business, wants to make a decision, or take some action based on making sense of some data. Organisations are becoming increasingly data driven, and despite the evolution of Business Intelligence, the ability of an organisation to derive value from data will be key to its success.

[1]: http://en.wikipedia.org/wiki/Extract,_transform,_load "ETL"
[2]: http://en.wikipedia.org/wiki/R_(programming_language) "R"