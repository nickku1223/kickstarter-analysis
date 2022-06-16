# Kickstarting with Excel

## Overview of Project

### Some campaigns in the theater category reached (or close to) their goals with short amount of time, we would like to know how the relation between the launch dates, the goals and the outcomes.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
[Outcomes Based on Launch Date] !(Theater_Outcomes_vs_Launch.png)

First, I use the dataset to create an pivot table, so I can better filter out the data for the purpose of this analysis. We want to see the relation between the outcomes and launch dates, so I put the outcomes to the columns field, data created conversion to the rows field, and removed the quarters and years that was automatically generated so I have months for rows. And outcomes to the values field, and put years and parent category to the filter field. Because we want to see the theater category we choose theater in the parent category filter, and filter the column labels only for successful, failed, and canceled.

Based on the data generated, I created a line chart for us to see the trend. With the chart, we can easily see that during summer time, especially May and June, have significant more successful cases, where the winter time, especially November and December, have the lowest numbers,


### Analysis of Outcomes Based on Goals

First, I created a new worksheet and give the proper headers in columns and different range of goals in rows, next I used the COUNTIFS function to help me find out the numbers for the successful, failed, and canceled campaigns, also to narrow it down to the "plays" subcategory, for the Number Successful where goal is less than $1,000, I used the following formula: 

=COUNTIFS(Kickstarters!D:D, "<1000", Kickstarters!F:F, "successful", Kickstarters!R:R, "plays") 

and get the result of 141, and applied the formula with some changes in order to find the Number Failed, Number Canceled.

After getting the numbers of the successful, failed and canceled, I used the SUM() function to add the 3 numbers to get the number of Total Projects, and get the percentage of successful, failed, and canceled by using the respective numbers divided by the Total Projects number.

With the data generated, I used the line chart tool to create a line chart for us to better see the trend, where I adjusted the range of Goals for the x-axis; percentage as the y-axis.

### Challenges and Difficulties Encountered

For the Outcomes Based on Goals, the challenging part can be when create a pivot table, to put the right field names to the right place, it can be confusing, and if we get the wrong fields then we might get the data that's not helpful for the purpose of this pivot table, took me a few tries and adding and deleting things around to get the data that I need.

For the Outcomes Based on Goals, the most challenging part is for me to figure out the correct syntax for COUNTIFS function, took me a few tries and research to find out where my formula was wrong (which is put criteria without the ""), and also the multiple conditions made the formula rather long, so if typing by hand it's easy to make mistakes. Once I figure out the formula and checked for any errors for the COUNTIFS function, the rest seem much easier, with a bit of exploring with the chart options, I got the data and chart that I needed.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

From the Outcome Based on Launch Dates data we can see that May and June has the highest successful campaigns, where November and December have the lowest, so May and June will be a good time to launch. On the other hand, can limit or reduce campaigns launch during November and December.



- What can you conclude about the Outcomes based on Goals?

From the Outcomes Based on Goals data we can see that the goals ranging from less than $1,000 to up to $20,000 have higher successful cases, and the range from $1,000 to less than $9,000 have the highest successful rates (more than 70%), so it will be good to set goal under $20,000 mark to have a better chance for the campaign to be successful.


- What are some limitations of this dataset?

We can see the higher and lower successful rates based on launch dates, but lack of information behind it, we can guess during the summer because of the weather/vacation time, it has higher successful rates, and during the winter time because of the weather/holiday people might less willing to donate, but without the data, we can't be sure, therefore, we can't really make informed, data-driven decisions.


- What are some other possible tables and/or graphs that we could create?

With the Outcomes based on Launch Dates data, we used the parent category of theater, and Outcomes Based on Goals data we have the subcategory of plays, we can create another table and graph for the subcategory musical and compare how the musical category perform vs the plays category.
