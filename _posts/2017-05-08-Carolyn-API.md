---
layout: post
title:  "Criminal sexual assault trends in Chicago, 2001-2017"
date:   2017-05-17
author: Carolyn Cakir
---

For this assignment, I chose to look at criminal sexual assault in Chicago from 2001 to 2017. I used the [Chicago Data Portal]( https://data.cityofchicago.org/Public-Safety/Crimes-2017/d62x-nvdr) as my dataset.

First, I got the total number of crimes per year by grouping the data. For this I used the query “https://data.cityofchicago.org/resource/6zsd-86xi.json?$select=year, count(*) as total&$group=year&$order=year.”
 Then I did the same grouping but filtered out all other crimes so that I got the total number of criminal sexual assaults per year, using the query “https://data.cityofchicago.org/resource/6zsd-86xi.json?$select=year, count(*) as total&$group=year&$order=year&primary_type=CRIM SEXUAL ASSAULT.” Using pivot tables to add and divide the totals, I found that criminal sexual assault accounts for 4 in every 1000 criminal cases brought up in the last 16 years. However, when you break that number down by year, criminal assault cases have risen in the City of Chicago. From 2014 and 2015, 5 out of every 1,000 cases were instances of criminal sexual assault, and in 2016 and the first few months of 2017, 6 out of 1,000 cases were criminal sexual assaults. This data would show that either there are more criminal sexual assaults occurring or more people are reporting criminal sexual assaults to the Chicago police.

Next, I wanted to find out how many of these cases resulted in arrest per year. After some work, I developed the query “https://data.cityofchicago.org/resource/6zsd-86xi.json?primary_type=CRIM SEXUAL ASSAULT&$select=arrest, count (*) as total&$group=arrest&$where=year=2017,” using a different $where for each year from 2001 to 2017.
Then, I used pivot tables to divide the number of arrests per year by the number of cases. This showed that only 16% of criminal sexual assault cases resulted in arrest over the past 16 years in Chicago, and that number is declining. In 2016, only 7% of criminal assault cases resulted in arrest. This number shows that it getting more unlikely that a criminal sexual assault would lead to an arrest in Chicago.
