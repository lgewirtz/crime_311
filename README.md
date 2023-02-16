# crime_311

This issue investigates the relationship between crime and 311 Service Requests in LA city neighborhood councils. Because I wanted to look at a year before COVID, I subsetted both datasets to the year 2019.

To explore correlation it was necessary to merge crime and Service Request datasets. First I tried using the variable PolicePrecinct but the merge failed because merge keys were not unique.  Second, I tried merging on 2 columns, 'PolicePrecinct', 'CreatedDate', and the merge didn't error out but the resulting dataset ended up with many more rows than the original Service Request dataset (the larger of the 2 datasets), showing that the merge keys were still not unique.

Finally I turned key variables into dummy variables and grouped them, thereby guaranteeing uniqueness. After a successful merge, I explored he correlation between the number of Service Request calls (Sum of NC_IDs) and 2 Crime variables ASSAULT_DEADLY_WEAPON and BATTERY_SIMPLE_ASSAULT using scatterplot with regression line.  The result is that there is very little to no correlation.
