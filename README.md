# Theater Kickstarter Analysis

## Overview of Project

### After nearly meeting her fundraising goal for her new play _Fever_, Louise requested information on the outcomes of other plays according to their fundraising launch dates and funding goals. The analysis that follows will help Louise determine the best month to start a fundraising plan and the monetary goal with the most likely success for future plays.

## Analysis and Challenges

### Starting with a data set of Kickstarter campaigns from 2009 to 2017 across 21 countries and a wide variety of categories, the YEAR function was used to extract the year each project was started from the "Date Created Conversion" column. Next, a pivot table was created and filtered showing successful, failed, and canceled theatrical projects according to the month of the year fundraising began. More specifically, "Date Created Conversion" was selected for the rows, "outcomes" was selected for the columns, and "Years" and "Parent Category" were chosen as filters. Blanks were filtered out of the data and the columns were sorted to show the successful data first followed by failed and canceled. Finally, the "Parent Category" was filtered to only display "theater".  The line graph shown below was created out of this pivot table data.
<img width="331" alt="Theater_Outcomes_vs_Launch" src="https://user-images.githubusercontent.com/102757676/161559435-80c37237-ffe7-4911-92ef-d55d9e0ffe68.png">


### Taking the large Kickstarter campaign data set and extracting the number of successful, failed, and canceled play projects along with their funding goals divided into 12 monetary ranges from less than $1000 to greater than $50,0000, a new table was created. In order to determine the number of successful, failed, and cancelled projects, the COUTIFS function was used. For successful plays with a fundraising goal of less than $1000, the following function was used: =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$R:$R,"plays",Kickstarter!$F:$F,"successful"). Column D of the Kickstarter data sheet contains the monetary goal value, column R contains the subcategory data of which "plays" was extracted, and column F contains the outcome of the project. Additionally, this function was utilized for each monetary goal range and per outcome of failed and canceled. Using the SUM function for the successful, failed, and canceled columns, the total projects was determined for each goal range. From the created table, the percentage of total projects that were successfull, failed, and canceled were charted on the line chart below based on their fundraising goals.
<img width="396" alt="Outcomes_vs_Goals" src="https://user-images.githubusercontent.com/102757676/161559201-945c0606-6caf-4847-ba2c-ad1d21830174.png">

### Challenges and Difficulties Encountered

## Results

- The "Outcomes by Launch Month" line graph created reveals that the highest number of successful theater projects were started in the month of May, followed closely by the month of June. December turned out to be the month with the lowest success rate, followed closely by January, March, and November. It is of note that the month of October revealed to have the fifth highest number of projects started, but with the highest failure rate (43%) out of all months. To conclude, May and June are the best months to start a fundraising campaign for a theater project. 

- The "Outcomes Based on Goals" line chart revealed that projects with a fundraising goal of less than $1000 were the most successful with a success rate of 76%. Projects with a fundraising goal of $1000 to $4999 performed nearly as successfully at 73% success rate. The least successful projects, with a 0% success rate, were those with a goal of $45,000 to $49,000, followed closely by projects with a goal of greater than $50,000 (13% success rate). It is also important to note that projects with a goal of $25,000 to $34,999 had very low success rates as well. One more note, no play projects started were canceled. To conclude, a fundraising goal of less than $5000 will have the greatest likelihood of success.

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
