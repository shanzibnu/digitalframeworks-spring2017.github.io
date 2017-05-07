---
layout: post
title:  "Spacewalk Competition"
date:   2017-05-08
author: Aileen Chuang
---

_This is an analysis of a [dataset](https://data.nasa.gov/Raw-Data/Extra-vehicular-Activity-EVA-US-and-Russia/9kcy-zwvn) from NASA._

Space exploration served as a dramatic arena for the United States and Russia to compete, especially during the Cold War. The dataset from NASA showed the numbers of the Extravehicular Activities, spacewalks, between the two countries since the Soviet Cosmonaut – Alexi Leonov – became the first human to conduct an EVA on March 18, 1965.

Updated in April 2015, NASA said the U.S. has conducted 236 spacewalks since 1965, while Russia has done 139.

<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/11MvR4YgIegRUpcJHkUipI4sYjuEit45n3m5WqrKebcs/pubchart?oid=931686000&amp;format=interactive"></iframe>

The U.S. caught up with Russia’s record in spacewalk in the same year on June 3, when Ed White ventured outside of his spacecraft. The American profile in EVA mission started to build up in the 1970s, conducting an average of 7.5 times of spacewalk every year.

<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/11MvR4YgIegRUpcJHkUipI4sYjuEit45n3m5WqrKebcs/pubchart?oid=436267471&amp;format=interactive"></iframe>

In the post-Cold War era, the U.S. has a growing number of spacewalk as in 2001, it peaked to 13, and in 2002, it had 19 activities.

While in Russia, the number of the spacewalk was higher in the 1990s, but not so much in the 2000s.

<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/11MvR4YgIegRUpcJHkUipI4sYjuEit45n3m5WqrKebcs/pubchart?oid=1084628964&amp;format=interactive"></iframe>

[Spreadsheet](https://docs.google.com/spreadsheets/d/11MvR4YgIegRUpcJHkUipI4sYjuEit45n3m5WqrKebcs/edit?usp=sharing)

API queries
1. Overall number:
https://data.nasa.gov/resource/eva.csv?$group=country&$select=country, count(*) as total
2. USA by year:
https://data.nasa.gov/resource/eva.csv?$select=date_trunc_y(date) as year, count(*) as total&$group=year&$where=country='USA'
3. Russia by year:
https://data.nasa.gov/resource/eva.csv?$select=date_trunc_y(date) as year, count(*) as total&$group=year&$where=country='Russia'
