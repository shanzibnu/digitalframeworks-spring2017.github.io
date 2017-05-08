---
layout: lesson
title:  "Web APIs and query languages"
description: "Use Postman (a utility for making structured HTTP requests) with the Socrata API (a web API) and the Socrata Query Langauge (a query language) to get summarized data."
class_date:   2017-04-24
author: David Eads
copyright: 'This lesson is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.'
---

## Overview

*Tools:* Socrata (city of Chicago open data portal version), Socrata Query Language (SoQL), Postman (a web browser-like tool for interacting with web APIs).

*Concepts:* Application programming interfaces (API), structured queries (select, filter, grouping, and aggregation), the request-response cycle.

*Philosophy:* Learning how to know what you need to learn next, how to understand enough to do what you need to do.

## Assignment

Read [In Defense of Interactive Graphics](https://www.vis4.net/blog/posts/in-defense-of-interactive-graphics/). 

Find a dataset on a Socrata open data portal. **[This list](https://docs.google.com/spreadsheets/d/1puYVFkALqr-4mnD4Pc2-54IfQe8-wACiZuRP4_BLJRg/edit#gid=1507239717)** of portals will be crucial.

The dataset should include a time-based field and, if possible, a categorical field or two.

Run at least two queries using the Socrata Open Data API and the [Socrata Query Language](https://dev.socrata.com/docs/queries/) using Postman. Your queries should include at least two of these parameters:

* A `$select` clause to pick the columns you wish to include in the exported data
* A `$groupby` clause to aggregate by a time or categorical field
* A `$where` clause to filter the data

You might want to use an `$order` clause to get more usable output, but you can also do this in your spreadsheet tool.

Import the datasets you downloaded into a Google Sheets spreadsheet and write a short blog post or create a short video describing what you found like you did for lesson 2. Link to both your spreadsheet and your original API queries at the end of your post.

With any luck, you'll be equipped with a strong and useful dataset to visualize next week.

## Lesson

[The NICAR Hitchhiker's Guide to Web APIs](https://docs.google.com/presentation/d/1jkZEcmgR5UeVzAvPskeZrlUH1tvXHXC9mo1NS-BWPvQ/edit#slide=id.p) by David Eads.
