layout: post
title:  "DC Charter School Data"
date:   2017-05-07
author: Nia Prater
---
For the web API assignment, I worked with a dataset from the DC Public Charter School Board. The set I ended up choosing was entitled
"PCS Waitlists and Available Seats by School and Year". The link to said dataset is here"(https://data.dcpcsb.org/resource/gi8f-g6am.json?)

I decided to run a query on the data that showed me how many total wait list spots there were for each school year.  The concept of the
assignment made sense, but it took me a few hours to figure out the exact query language I needed to get the results I wanted. Eventually,
I got it. First, I put the key $select into Postman followed by the value school_year, sum(total_number_of_names_on_the_wait_list). Next, I inserted the key $group with the value school_year.

These keys and values eventually gave me the data I needed. I discovered that DC Public Charter Schools had 18,456 names on the waitlist in 2014-2015, 18,877 names in 2015-2016 and finally 20,880 in 2016-2017. This data clearly shows a yearly increase of families wanting to send their kids to charter schools. The reason why could be a story!

The URL of my final query was "this"(https://data.dcpcsb.org/resource/gi8f-g6am.json?$select= school_year, sum(total_number_of_names_on_the_wait_list)&$group=school_year)


Next, I ran a query to find out how many available seats there were each year. To do this, I put the key $select in follwed by the value school_year, sum(total_number_of_seats_available). Then, I had the key $group with the value school_year. This query showed me that there were 2,618 available seats for students in 2014-2015 and 3,215 seats in 2015-2016. No number came up for 2016-2017, I assume because it's data that is still being collected.

My URL for this query was: https://data.dcpcsb.org/resource/gi8f-g6am.json?$select=school_year, sum(total_number_of_seats_avai lable)&$group=school_year 

Here is my "spreadsheet"(https://docs.google.com/spreadsheets/d/1PKGd2sL3_3ROY1jDYO2RIQp64PRrBkcT2zdwsx5Vk4s/edit?usp=sharing)
