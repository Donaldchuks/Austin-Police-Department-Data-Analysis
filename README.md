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

‘Month’: Extracted from the Response Datetime column to analyze monthly trends in response times and call volumes.

‘Time of Day’: Derived from the Response Hour column, The “Time Of Day” column was categorized into four distinct periods: Morning (6 AM to 12 PM), Afternoon (12 PM to 6 PM), Evening (6 PM to 12 AM), and Night (12 AM to 6 AM). This classification provided insight into temporal patterns.

- Renamed 'Incident Number' to 'Call Volume': In this dataset, each incident is assigned a unique "Incident Number." So, when we count the number of incident numbers, we're essentially counting the number of individual 911 calls.

- Used the 'Council District' column for geographic analysis: This column provides a more relevant level of geographic detail compared to 'Geo ID' for analyzing district-level trends.

- Utilized the "Final Problem Category" column as the “Call reason” for analysis: This column provides a more accurate and specific categorization of incidents, as it describes the ultimate issue addressed by the APD incident in contrast to the ”Initial Problem Description” column, which may change based on additional information gathered during the call-taking and response processes.

These adjustments enabled more precise analysis and visualization of our dataset, ultimately providing valuable insights into 911 call patterns and response times.

Once the new columns were added, the dataset was imported into Power BI, setting the stage for comprehensive data visualization and analysis.

## ANALYSIS : UNVEILING THE SECRET OF OUR DATA
Now that our data is prepared, we embark on a detailed analysis to uncover key insights. This analysis is divided into five key sections:

1. Overview
2. Response Time Overview A general look at how quickly APD responds to calls.
3. Calls Trend Overview: How call volumes vary throughout the day, week, and month.
4. Patrol Sector Performance: A comparison of response times across different patrol sectors.
5. Geographic Patterns: Analyzing response times in different neighborhoods and districts.

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

