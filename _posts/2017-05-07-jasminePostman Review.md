---
layout: post
title:  "Oakland Crimes in 90 days"
date:   2017-05-07
author: Jasmine Minor
---

_This is an analysis of a [dataset](https://data.oaklandnet.com/Public-Safety/CrimeWatch-Maps-Past-90-Days/ym6k-rx7a/data) from the City of Oakland Datasets_

This week, I chose to explore crime committed in the last 90 days in Oakland, California. I decided to begin with how many different types of crime had been reported. After filtering through some of the datasheet, I found an interest in domestic violence cases.

Domestic violence led the way with 659 reports in the last 90 days.

Since this caught my attention, I chose to explore further. I found that out of those 659 reports, 478 were considered spousal battery/abuse with 40 cases happening in the last month.

<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/u/1/d/1bBq7q257tfKcRSxShIwNvxnq8USdD12rDDExD0bhWOQ/pubchart?oid=1496178475&format=interactive"></iframe>

Police beat 04X had by far the most crimes covered with 431 reports with 27 of those being domestic violence crimes.

<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/u/1/d/1DmQAUYIFJteJohHXnZ5RWVQYwNP8wloREhin75YD_vw/pubchart?oid=1840009112&format=interactive"></iframe>


Out of my own curiosity, I decided to google “domestic violence in Oakland.” To my surprise there are only two law centers that deal directly with family violence in the downtown area. Only four exist total for the entire city. When I looked at some of the recent news surrounding this issue, I discovered the May Day march focused largely on it with many immigrants not coming forward for help due to fears of deportation.

Unfortunately, the dataset I have only goes back the last 90 days. I would be interested in finding out if domestic violence increased since President Trump took office. Under circumstances that an immigrant-heavy city would have many afraid to come forward, I wonder if perpetrators might feel more inclined to commit the crime and if the 659 reports is actually a low number for what is happening.

["Spreadsheet"](https://docs.google.com/spreadsheets/d/1bBq7q257tfKcRSxShIwNvxnq8USdD12rDDExD0bhWOQ/edit#gid=165080352).

API Queries:
1. Count of Domestic Violence reports https://data.oaklandnet.com/resource/3xav-7geq.json?crimetype=DOMESTIC VIOLENCE&$select=crimetype, count (*) as total&$group=crimetype
2. Types of Domestic Violence reports	https://data.oaklandnet.com/resource/3xav-7geq.json?crimetype=DOMESTIC VIOLENCE&$select=description, count (*) as total&$group=description&$where=date
3. Police beats with most Domestic Violence	https://data.oaklandnet.com/resource/3xav-7geq.json?policebeat=04X&$order=crimetype&crimetype=DOMESTIC VIOLENCE




>>>>>>> origin/master
