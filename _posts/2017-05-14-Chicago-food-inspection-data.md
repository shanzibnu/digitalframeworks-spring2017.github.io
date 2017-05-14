---
layout: post
title:  What's going on at Chicago eateries?
date:   2017-05-14
author: Maryam Saleh
---

One in five Chicago food establishments inspected by the Department of Public Health failed their inspections this year, according to publicly available data. Of the 1,261 eateries that failed to meet food safety standards, 997 were found to have high-risk health violations.

Sixty-five eateries in the 60625 zip code, which includes Albany Park, Lincoln Square, Ravenswood, and Ravenswood Manor, failed their inspections—more than in any other part of the city. The glitzy Gold Coast neighborhood, represented by zip codes 60610 and 60611, is home to 25 inspection failures. In the 60611, which also includes the Magnificent Mile, alone, 17 dining places have failed their food inspections so far in 2017.  

A failing result means that inspectors from the Department of Public Health’s Food Protection Program found critical or serious violations that could not be fixed during the inspection, according to [information](https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF) provided online by the City of Chicago. We’ll need to talk to someone from that office, though, to figure out types of mistakes are considered critical, and to better understand how the risk assessment of the violations is done.

Of the food establishments that failed their inspections between January 1 and May 13, 2017, 859 were restaurants, 131 were schools, 126 were grocery stores, and 12 were daycares. But don’t stop eating out on account of this data; it’s not all bad news! The pass rates in those categories are 2,512 restaurants, 372 schools, 328 grocery stores, and 54 daycares—and those numbers don’t account for places that passed “with conditions.” That means the establishments were found to have serious violations, but that the violations were fixed during the inspection visit.  

If you’re interested in learning whether a restaurant you eat at has been found in violation of food safety codes, check out [this](https://data.cityofchicago.org/Health-Human-Services/Food-Inspections/2bnm-jnvb) data set. The information goes back to 2010. Happy dining, folks!

Check out my Google spreadsheet with the data [here](https://docs.google.com/spreadsheets/d/1vDn6IuseqNEPTaCHPNRTO6_ZM8DTDlRAophIs-hd-LQ/edit?usp=sharing).

These are the API links I used for my analysis:

https://data.cityofchicago.org/resource/cwig-ma7x.csv?$group=results&$select=results, count(*) as total&$where=inspection_date > "2017-01-01"

https://data.cityofchicago.org/resource/cwig-ma7x.csv?$group=results&$select=results, count(*) as total&$where=risk = "Risk 1 (High)" and inspection_date > "2017-01-01"

https://data.cityofchicago.org/resource/cwig-ma7x.csv?$group=zip&$select=zip, count(*) as total&$where=results = "Fail" and inspection_date > "2017-01-01"

https://data.cityofchicago.org/resource/cwig-ma7x.csv?$group=results&$select=results, count(*) as total&$where=facility_type = "School" and inspection_date > "2017-01-01"

https://data.cityofchicago.org/resource/cwig-ma7x.csv?$group=results&$select=results, count(*) as total&$where=facility_type = "Restaurant" and inspection_date > "2017-01-01"

https://data.cityofchicago.org/resource/cwig-ma7x.csv?$group=results&$select=results, count(*) as total&$where=facility_type = "Grocery Store" and inspection_date > "2017-01-01"

https://data.cityofchicago.org/resource/cwig-ma7x.csv?$group=results&$select=results, count(*) as total&$where=facility_type = "Daycare Above and Under 2 Years" and inspection_date > "2017-01-01"
