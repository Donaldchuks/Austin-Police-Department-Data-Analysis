## INTRODUCTION
In the midst of chaos, a single phone call can be the difference between life and death. For the men and women who answer 911 calls, every moment counts. But what if we could uncover patterns and insights within these critical moments to improve response times and save more lives?

I dug into nearly 96,000 911 calls received by the Austin Police Department to find out. What I discovered has the potential to transform emergency response in Austin and beyond.

This report presents an in-depth analysis of 911 call data from the Austin Police Department (APD). By examining key metrics such as response times, incident types, and geographic patterns, this analysis aims to uncover actionable insights to improve resource allocation and operational efficiency.
The ultimate goal is to provide recommendations backed by evidence to enhance APD’s ability to respond to emergencies promptly by reducing response times and ensuring a safer community for all.

## PROBLEM STATEMENT 
Despite the high volume of 911 calls, ensuring timely and effective responses remains a critical challenge for the Austin Police Department. As part of my portfolio project, this analysis is focused on analyzing a subset of 96,000 911 calls to identify patterns and trends that can inform resource allocation and optimization.

## RESEARCH QUESTIONS
For this project, I addressed questions that were specifically asked in the provided dataset aimed at improving response times. The questions I explored are:

1. Which types of emergencies tend to have slower response times, especially during peak traffic hours?

2. Which patrol sectors generate the most traffic and have the fastest/slowest response times?

3. How do response times vary by priority level for different incident types?

4. For each day of the week, calculate the difference between the average response time for that day and the average response time for all days combined

5. What is the average response time for all incidents involving mental health issues?

6. Which neighborhoods or areas of the city generate the most emergency calls, and what are the average response times for these areas?

## ABOUT DATASET.
The provided data set consist of just one csv file which contains one table and the following columns:
1. Incident Number: Unique identifier for each incident.
2. Incident Type: Type of incident (dispatched or officer-initiated).
3. Mental Health Flag: Indicates if the incident is mental health-related.
4. Priority Level: Priority level assigned to the incident (0-4) with 0 being the highest priority and        4 being the lowest priority.
5. Response Datetime: Date and time the 911 call was answered.
6. Response Day of Week: Day of the week the response occurred.
7. Response Hour: Hour of the day the response occurred.
8. First Unit Arrived Datetime: Date and time the first unit arrived on scene.
9. Call Closed Datetime: Date and time the incident was closed.
10. Sector: Patrol sector where the incident occurred.
11. Initial Problem Description: Preliminary description of the problem.
12. Initial Problem Category: General category describing the problem.
13. Final Problem Description: Description of the ultimate issue addressed.
14. Final Problem Category: General category describing the ultimate issue.
15. Number of Units Arrived: Number of APD units that arrived on scene.
16. Unit Time on Scene: Total time spent on scene by all APD units.
17. Call Disposition Description: Description of the outcome of the call.
18. Report Written Flag: Indicates if a report was written for the incident.
19. Response Time: Time between call answer and first unit arrival(In Sec)
20. Officer Injured/Killed Count: Number of officers injured or killed.
21. Subject Injured/Killed Count: Number of subjects injured or killed.
22. Other Injured/Killed Count: Number of others injured or killed.
23. Geo ID: Census Block Group identifier.
24. Census Block Group: Shortened Block Group Name.
25. Council District: Council district where the offense occurred.

## DATA TOOLS
Excel - Cleaning Dataset

Power BI - Creating Reports

## DATA MANIPULATION AND PREPARATION
The dataset was provided as a clean CSV file containing one Table of approximately 96,000 911 call records, with each record representing a unique incident and 25 columns. No missing values or duplicates were found upon review. However, I enhanced the dataset to facilitate deeper analysis and answer time-based questions, such as trends over specific periods or time of day.
To enhance the dataset and facilitate deeper analysis, I made the following adjustments:
- Created two additional columns

**‘Month’:** Extracted from the **Response Datetime** column to analyze monthly trends in response times and call volumes.

**‘Time of Day’:** Derived from the **Response Hour** column, The “Time Of Day” column was categorized into four distinct periods: Morning (6 AM to 12 PM), Afternoon (12 PM to 6 PM), Evening (6 PM to 12 AM), and Night (12 AM to 6 AM). This classification provided insight into temporal patterns.

**- Renamed 'Incident Number' to 'Call Volume':** In this dataset, each incident is assigned a unique "Incident Number." So, when we count the number of incident numbers, we're essentially counting the number of individual 911 calls.

**- Used the 'Council District' column for geographic analysis:** This column provides a more relevant level of geographic detail compared to 'Geo ID' for analyzing district-level trends.

**- Utilized the "Final Problem Category" column as the “Call reason” for analysis:** This column provides a more accurate and specific categorization of incidents, as it describes the ultimate issue addressed by the APD incident in contrast to the ”Initial Problem Description” column, which may change based on additional information gathered during the call-taking and response processes.

These adjustments enabled more precise analysis and visualization of our dataset, ultimately providing valuable insights into 911 call patterns and response times.

Once the new columns were added, the dataset was imported into Power BI, setting the stage for comprehensive data visualization and analysis.

## ANALYSIS : UNVEILING THE SECRET OF OUR DATA
Now that our data is prepared, we embark on a detailed analysis to uncover key insights. This analysis is divided into five key sections:

**1. Overview**
**2. Response Time Overview:** A general look at how quickly APD responds to calls.
**3. Calls Trend Overview:** How call volumes vary throughout the day, week, and month.
**4. Patrol Sector Performance:** A comparison of response times across different patrol sectors.
**5. Geographic Patterns:** Analyzing response times in different neighborhoods and districts.

## OVERVIEW
This page displays a summary of key metrics such as 
- Filter Panel: Allows users to filter data based on call type and location, enabling more targeted analysis.
- Total Call Vol: A clear picture of the overall call volume, indicating the demand on emergency services.
- Avg Response Time: The average response time for all the calls which  measure the overall efficiency in responding to calls.
- Total patrol sectors: the total patrol sectors in austin department
- Mental Health response time: Provides specific insights into the department's response to mental health-related calls.
- Call Volume Trends: Visualizes call volume trends over time, helping identify peak hours, days, and months.
- Avg Response Time Trend: Reveals when response times are typically slower, allowing for proactive resource allocation and potential staffing adjustments.
- Average Response Time Per Call: Compares average response times per call across the different patrol sectors.
- Average Response Time: Priority Level:   Examines how response times vary based on call priority. 
- Incident trends by priority level: Displays the number of incidents over time for each priority level.
- Top 5 Busiest Districts: Identifies the top five busiest council districts, allowing for focused resource allocation and improved response strategies.

## RESPONSE TIME OVERVIEW
This page gives insight into response time trends, focusing on various temporal operational factors such as
- Average Response Time: A key performance indicator (KPI) showing the overall average response time for all calls.
- Avg Response Time For Mental Health Incidents: A key performance indicator (KPI) highlighting the average response time for mental health-related calls.
- Average Response Time for priority level: Examines how response times vary based on call priority.
- Average Response Time Difference by Day: Compares the average response time for each day of the week to the overall average response time.
- Average Response Time Weekly: Compares average response times across different days of the week.
- Average Response Time Period of Day: Analyzes how response times vary across different periods of the day (e.g., morning, afternoon, evening, night). This reveals peak hours for emergency calls and informs staffing decisions.
- Average Response Time Monthly: Tracks average response times across different months of the year.

## CALL TREND OVERVIEW
This page provides a comprehensive overview of call volume and trends related to 911 incidents in Austin.
- Total Calls Received: A key metric displaying the total number of 911 calls received by the department.
- Call Trends by Priority Level: This line chart visualizes the number of calls received over time for each priority level. 
- Total Calls Received by Patrol Sector: This funnel chart visualizes the distribution of calls across different patrol sectors, ranking them from the sector with the highest call volume to the sector with the lowest.
- Count of Incident Number by Month: Seasonal trends Identify months with higher or lower call volumes.
- Call Type Metrics: A table that shows each particular call type, call volume and their Avg response time.

## PATROL SECTOR PERFORMANCE
**For this visual, I created a new measure **“Avg Response Time Per Call”** by dividing the average response time by the incident count for each patrol sector.*

**This metric helps us understand how fast a patrol sector responds to each individual call, regardless of how many calls they receive. This is to ensure a fair comparison of response times across patrol sectors. This measure was necessary because sectors with higher incident volumes naturally tend to have higher total response times, which can be misleading.*
 
- Total Patrol Sectors: This KPI provides the total number of patrol sectors within the Austin Police Department.
- Average Response Time per Call: This KPI displays the overall average response time per call for all calls received.
- Total Calls Received by Patrol Sectors: This chart visualizes the distribution of calls across different patrol sectors, ranking them from the sector with the highest call volume to the sector with the lowest.
- Average Response Time per Call by Patrol Sector: This bar chart compares the average response time per call across different patrol sectors.
- Normal Avg Response Time Trend: This line chart compares the normal average response time trend with the actual response time trend for each patrol sector.
- Avg Response Time per Call Trend: This line chart visualizes the trend of average response time per call over time for each patrol sector. 

## GEOGRAPHIC PATTERNS
This page provides valuable insights into the district-level performance of the emergency response system.
- Total District: A KPI that provides the total number of districts within the city.
- Avg Response Time Trend Across Districts: Visualizes the trend of average response times across different districts over time.
- Count Of Sectors Per District: This shows the total number of patrol sectors attending to calls per district. 
- Avg Response Time Per District: This chart provides details on how fast each district performed in responding to calls.
- Top 5 Busiest Districts: Identifies the top five busiest districts based on call volume and displays their associated average response times.
  
## OBSERVATIONS
**1. Response Time Performance:**
**- Overall Response Time:** The overall average response time for all calls was 3.01k seconds (approximately 50 minutes).
**- Priority Level Impact:** As expected, higher-priority incidents (levels 0 and 1) had shorter response times (604 seconds and 875 seconds, respectively) compared to lower-priority calls. This indicates that the department is generally effective in prioritizing critical incidents.
**- Mental Health Response Times:** The average response time for mental health-related incidents (3.38k seconds) was notably higher than the overall average, suggesting we need to find ways to improve how we handle these situations.
**- Time of Day Variations:** Response times were generally faster during the night (2719 seconds) compared to other periods of the day, likely because traffic was lighter.
**- Day-of-Week Variations:** Response times were fastest on Fridays (2598 seconds) and slowest on Saturdays (3508 seconds), likely influenced by factors such as increased weekend traffic or higher call volume on Saturdays.

**2. Call Volume Trends:**
**- Seasonal Variations:** We saw clear seasonal patterns in call volume, with higher call volumes observed during the summer months (June, July, August) compared to the winter months. This might have been due to increased outdoor activities and seasonal events during the summer.
**- Daily Trends:** Call volume peaked during the afternoon (28.22k calls) and evening (19.02k calls) periods, reflecting increased activity and potential for higher demand during these times.
**- Weekday Variations:** Weekdays were generally busier than weekends, with Monday, Tuesday, and Wednesday being the busiest days.

**- 3. Sector-Level Performance:**
**- Call Volume Distribution:** Some sectors had a much higher volume of calls than others. Sectors like Henry, Edwards, and Frank consistently received a higher volume of calls.
**- Response Time Analysis:** To compare how quickly sectors respond, we used a special metric called "Average Response Time per Call." Like I stated earlier, this metric helps us understand how fast a sector responds to each individual call, regardless of how many calls they receive.
**-    Think of it this way:**
Imagine two sectors. Sector A receives 100 calls and takes an average of 300 seconds to respond to each. Sector B receives 50 calls and takes an average of 200 seconds per call. Sector B might have a lower overall response time, but it's handling fewer calls. "Average Response Time per Call" helps us see that Sector A is actually responding more quickly to each individual call.

This analysis revealed that sectors like David, Baker and George demonstrated shorter average response times per call.
- Sectors with higher "Average Response Time per Call" may need closer attention. This could indicate potential issues like insufficient resources, operational challenges, or difficulties navigating the area.

**4. District-Level Analysis:**
**- Busiest Districts:** Council Districts 1, 9, and 3 consistently ranked among the top five busiest districts, indicating a higher demand for emergency services in these areas.
**- District Performance:** The data shows that some districts have significantly slower normal average response times. For example, Council District 1 has a normal average response time of 3319 seconds. Notably, Council District 1 is covered by 5 sectors, which is one of the highest sector allocations. In contrast, Council District 9 has a faster normal average response time and is also covered by 6 sectors. On the other hand, districts with fewer sectors, such as District 6 (2 sectors) and District 10 (2 sectors), have relatively slower response times. This suggests that sector allocation may be a factor influencing response times, but it's not the only factor.


## RECOMMENDATIONS 
Here are some recommendations based on the observation from the analysed dataset
**1. Learn from the Best:**
 Taking a closer look at sectors like David and baker which have the fastest normal average response time despite having high call volumes.. What's their secret? Identify the strategies and best practices that contribute to their success and apply them to underperforming sectors.
**Investigate and Address Underperforming Sectors:** Analyze sectors with higher "Average Response Time per Call," even with lower call volumes. Investigate potential factors contributing to slower response times, such as resource constraints, operational challenges, or geographical limitations.
**2. Tackle High-Volume Districts:**
 Council Districts 1, 3, 4, and 7 have slower response times and high call volumes. Our analysis reveals a clear pattern, districts with more patrol sectors responding to incidents tend to have faster response times. A clear example of this is district 0 and 9, which have the highest patrol sector allocation and consequently boast the fastest response times. This insight should inform the approach to districts struggling with slow response times. To get them back on track, APD should consider reallocating existing resources or adding additional officers and dispatchers to these districts to improve response times
**3. Optimize Staffing and Scheduling:**
A. Adjust Staffing Levels Based On Season - We saw clear seasonal patterns in call volume as call volumes consistently spike during the summer months (June, July, and August) compared to the winter months, likely due to increased outdoor activities and seasonal events. To ensure readiness to respond effectively, APD should adjust the number of officers on duty based on the time of year. There should be an increase in staffing during busier summer months and a slight reduction during quieter winter months to make the best use of resources.
B. Adjust Staffing Levels Based on Time of Day and Day of Week - Call volumes and response times vary significantly by time of day and day of week. For example:
-     Monday, Tuesday, and Wednesday have the highest call volumes while Afternoon periods experience a 28% increase in call volume compared to morning periods.
-     Saturdays have the slowest average response time and a relatively high call volume 
**To address these variations, consider adjusting staffing levels as follows:**
- Increase staffing by 10-15% on Mondays, Tuesdays, and Wednesdays to address higher call volumes.
- Add additional dispatchers and officers during afternoon periods to handle increased call volume.
- Review staffing levels on Saturdays and consider adding additional resources to improve response times.
**4. Enhance Response Times for Mental Health Incidents:** The average response time for mental health-related incidents (3.38k seconds) was notably higher than the overall average. Develop strategies to reduce response times for these incidents, such as providing specialized training for responders, partnering with mental health professionals or creating a dedicated crisis response team dedicated to mental health response.
**5. Implement Technology Enhancements:** Leverage technology, such as automated dispatch systems and data analytics tools, to streamline emergency response processes and improve response times.
**6. Foster Community Partnerships:** Forging strong partnerships with local organizations, mental health services, and other stakeholders could help us better support our community during emergencies and improve outcomes for everyone.

## SUMMARY
As I reflect on the insights gained from analyzing 96,000 911 calls, I'm reminded of the immense responsibility that emergency responders carry every day. With this report, I hope to contribute to the Austin Police Department's ongoing efforts to improve their response to emergencies.

My analysis led me to suggest some practical ways to enhance their operations, such as adjusting staffing levels to match peak demand, reallocating resources to areas with the greatest need, and exploring innovative technologies to streamline their work. I also propose that the APD consider developing specialized strategies for responding to mental health crises, potentially including a dedicated crisis response team.

Ultimately, this report is a humble attempt to support the APD's mission to serve and protect the community. By leveraging data and insights, I believe this analysis can help to reduce response times, enhance public safety, and ensure that emergency responders have the resources they need to do their vital work.

Thanks for reading.

