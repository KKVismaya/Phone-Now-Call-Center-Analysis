# Phone Now Call Center Analysis-Dashboard

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiOTc2MTgyZDMtZWY0Yi00ZWRjLWI4MWUtNjA5MDcyYTllMzA4IiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9

## Problem Statement

This dashboard helps the Call Center Manager understand transparency of the data they have at their Call Center. 

The Manager wants to know the accurate overview of long term trends in customer and agent behaviour.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 :The data is now all set to create the reports.
- Step 5 :We are asked to create the following measures could help to define proper KPIs:

  - Overall customer satisfaction
  - Overall calls answered/abandoned
  - Calls by time
  - Average speed of answer
  - Agent’s performance quadrant -> average handle time (talk duration) vs calls answered
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 :Calculated the count of total calls received by the company.

      Total Calls = COUNT(Table1[Call Id])
    

 - Step 8 :Calculated the Average answering speed of the calls by the agents.

      Avg Answering Speed = AVERAGE(Table1[Speed of answer in seconds])

- Step 9 :Calculated the total number of  calls answered by the agents.

      Total Calls Answered = COUNTX(FILTER(Table1,Table1[Answered (Y/N)] = "Y"),Table1[Call Id])

Step 10 : Calculated the total number of calls resolved by the agents.

      Total Calls resolved = COUNTX(FILTER(Table1,Table1[Resolved]="Y"),Table1[Call Id])

- Step 11 : Visual filters (Slicers) were added for three fields named "months", "Date range" & "Resolved or not".
- Step 12 : Four card visuals were added to the canvas,  representing Total Calls, Average answering speed, Total calls answered and Total calls resolved.
         
- Step 13 : A clustered column chart was also added to the report design area representing the total number of calls answered Vs resolved by each agents.
- Step 14 :Two pie charts were also added to the report design area, one representing the total number of calls answered Vs resolved and another representing Total calls answered and total calls anandoned.
- Step 15 : Average performance rating was added to the card visual.
- Step 16 : A bar chart representing average call duration of each agents 

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.
It contained visuals like bar charts, column charts, poe charts, tree map  that gave the transparency and insights into the data of the call center.
