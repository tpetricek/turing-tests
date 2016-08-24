---
layout: post
number: "001"
title: "Butadiene: Comparison with health objective for 2003"
data-url: "tba"
---

## Background
The data set for this challenge consists of a single CSV file from the 
[UK Open Government Data portal](https://data.gov.uk/). The data set contains
annual means of measurements of 1,3-butadiene at a number of automatic sites
and provides comparison with health objective for 2003.
This challenge is an example of a "messy real-world CSV file". The file contains
table with data, but also various additional meta-data about the data set. 

### Data set preview 

![](2016-08-23-butadiene-heath-objectives/screenshot.png?)

## Tasks

 1. The main task is to automatically detect which part of the CSV file is 
   the data set and what is meta-data.
   
 2. We would like to detect that the data in columns labelled "1994" to "2010"
   are values for different places _except_ for the row "Count" (which is the
   count) and "AQS Objective" (which is a value, but without geographical 
   location). 
   
 3. Ideally, you would also detect that the "Site Name" column represents
   a geographical location, the column keys "1994" to "2010" represent
   years and (as a bonus) that the unit of the values in the table is annual 
   mean measured in `µg / m3`.

 4. Another thing to detect is that the empty cells in the table mean `N/A`
   (in particular, they cannot be automatically filled with zeros, because
   zero would be a valid value in the context of the table).
   
### Remarks

In the task 3 where we would like to detect that "Site Name" is a city and
"1993" to "2010" are years, you can report this information in the parsed data
via any machine-readable format of annotations you like. One option would be
to use the [schema.org](http://schema.org/) annotations and mark "Site Name"
as [City](http://schema.org/City) and years as [Date](http://schema.org/Date).

## License

The data set is available from [data.gov.uk](https://data.gov.uk/dataset/13-butadiene-running-annual-mean-at-automatic-sites-comparison-with-health-objective-for-2003-u-2010) under the 
[Open Government
License](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
