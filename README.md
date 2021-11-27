# kickstarter_analysis

## Overview of Project

### Purpose
Louise’s play Fever just missed her Kickstarter fundraising goal of $2,885 by only $400. She ran her campaign for 28 days between June and July. Now Louise would like to know how other campaigns faired based on their goals and launch date. In our analysis of the Kickstarter data, we will take a deeper look at Theater campaigns and determine what factors such as the time of the year that a campaign is executed, and the amount of campaign goal played in successful Kickstarter campaigns. Our goal is to provide Louise with better insights to apply to her next Kickstarter campaign in an effort to be successful in future fundraising efforts.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

Looking first at the Creation Date of the Kickstarter campaigns dataset, we compared those time frames and if the campaign achieved its fundraising goal. Using a pivot table, we can quickly filter the data by Parent Category which allows us to look at all Theater projects within the data set. Now we can look at the relation of successful and failed campaigns within the context of the month they were created.

![image](https://user-images.githubusercontent.com/93485455/143312331-92623ddf-5d1c-4fe7-9f72-3cc18b0921ea.png)

The months that not only had the most campaigns created but also the most successful ones were May and June.

![Screen Shot 2021-11-24 at 3 14 05 PM](https://user-images.githubusercontent.com/93485455/143663705-bb8b7e41-ea5a-4f48-80a8-ecf6887f972b.png)

To better illustrate this point, we created a chart called Theater Outcomes Based on Launch Date.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/93485455/143663724-37d325a2-33e0-4cc1-9fd8-91a7e1d5b574.png)

### Analysis of Outcomes Based on Goals

The second factor we wanted to analyze was the how the amount of the campaign goal correlated to how successful the campaign turned out. We decided to organize the dollar amounts starting with anything a $1,000 or less then range of $5,000 increments. It would require us to write a lengthy excel formula to address those ranges but also the other criteria needed to filter to get to the pertinent data. Here is the formula we used:

```
=COUNTIFS(Kickstarter!D$84:D$4108,">=1000",Kickstarter!D$84:D$4108,"<5000",Kickstarter!F$84:F$4108,"successful",Kickstarter!P$84:P$4108,"plays")
```
Utilizing the COUNTIFS function in excel, we were able to group the data by the ranges we wanted and the also filter the data by the criteria of what was 'successful' and subcategory type of 'plays'.

We continued to analyze the data further by determing the percentages successful and failed. Below is the data organized from our formulas:

![Screen Shot 2021-11-26 at 12 59 48 PM](https://user-images.githubusercontent.com/93485455/143621824-491113d5-0e4b-4482-bbef-b111a4c60c1d.png)

To better illustrate this point, we created a chart called Outcomes Based on Goals.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/93485455/143622437-e1c8f597-bc4b-4b1d-8ef7-5c57713dfaea.png)


### Challenges and Difficulties Encountered

In working with a large data set like the Kickstarter data, the biggest challenge was filtering the data and making sure as we worked through the data that it was understood if the data was filtered or not and if it was filtered properly. A few times the data did not reflect what was expected and it required a review of formuals used to determine the issue.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

From the analysis, our conclusion is that May and June were the best months to run a Kickstarter campaign. May and June had the most Plays campaigns started and ultimately the most succesful ones. While the data did show that the summer months (May - August) had the most campaigns created, based our chart, it clearly demonstrates that there is a trend of campaigns becoming less successful after June as the year progresses.

- What can you conclude about the Outcomes based on Goals?

From the analysis, our conclusion is that campaigns that had goals less than $5,000 were the most successful. Also there were more campaigns launched that had goals under $5,000 as well. 

- What are some limitations of this dataset?

Ideally, it would have been nice to have data that included the last few years as the last year in the dataset was 2017. It would also would have been enlightening to see what type of marketing and advertising that each campaign had. That could be a big factor in the difference of those that succeeded and those that failed within the less than $5,000 goal range.

- What are some other possible tables and/or graphs that we could create?

The deeper analysis with the existing dataset that could be proformed is exploring the length of the successful campaigns. Looking at the filtered data, Plays campaigns that ran exactly 30 days had a greatest amount of success. The chart below shows this point:

![Plays Campaigns in Days](https://user-images.githubusercontent.com/93485455/143642224-86363d52-a374-4546-bc18-bf6422086690.png)

Based off our earlier analysis, the next step we took was looking at Plays campaigns that ran 30 days and had goals that were less than $5,000.

![Screen Shot 2021-11-26 at 2 59 49 PM](https://user-images.githubusercontent.com/93485455/143644258-36ebf19a-9c4a-4d8f-bc18-8e398b066b8c.png)

From this table, we decided to look at the percentage of successful campaigns that ran for exactly 30 days and had goals of less than $5,000.

![Percentage of Plays Outcomes 30 Days](https://user-images.githubusercontent.com/93485455/143646534-71b82723-cb94-49ad-bf8f-98b14398acd6.png)

Within that same dataset, we took a long at the amount of campaigns that ran within the range of exaclty 30 days and less than $5,000.

![Screen Shot 2021-11-26 at 7 15 30 PM](https://user-images.githubusercontent.com/93485455/143663743-948894c1-b9a6-41b1-ab67-91f88c7bf425.png)

Lastly, taking this dataset we wanted to look at the idea of launch date, 30 days length, and less than $5,000 with Plays campaigns to see if we can focus in more on the best outcomes that Louise could possibly take into account in her next fundraising effort.

![Screen Shot 2021-11-26 at 7 13 09 PM](https://user-images.githubusercontent.com/93485455/143663739-2f0fd5cc-5442-4748-a97a-6755f3f006d8.png)

Our recommendation would be based on the data provided that Plays campaigns with Goals of Under $5K of 30 Days in Length Launched in May and June had the most success and would be the best aspects to model in future campaigns.
