# Customer Call Contact Volume Analysis - Power BI Dashboard - Tam Vu

DISCLAIMER: This is the project that I took the dataset from Kaggle. This data is about Customer Call Center Data. I came up with the idea of business case scenario. 

**Case scenario**: 
In light of Company Y's recent substantial growth, there is a noticeable awareness of the significance of customer retention alongside product development. The Senior Customer Delivery Manager aims to gain deeper insights into customer satisfaction rates, common topics or issues prompting customer engagement with the support call center, the level of assistance provided by specific agents, and the correlation between agent performance and high customer satisfaction scores. The purpose of this dashboard is to gain deeper insights from customer call volume data and offer actionable recommendations for strategic improvements.

**How I create this dashboard:**
**1. Using the Design Thinking Method to proceed initial ideas in building the dashboard**
- **Step 1: Empathize**
  + Stakeholder Challenge: "The customer delivery manager wants to improve their customer delivery's quality, especially with customer call center data. For example: how many calls the agents assisted, how satisfied customers are after their cases are solved, common problems from customers, satisfaction rate
  + **Dashboard Goal**: Providing more insights about the overview results of the customer call center team, the dashboard will help the key stakeholders create strategy more easily through data-driven decision-making.
  + Who will mainly use this report: Senior Customer Delivery Manager
  + **Dataset Understanding**:
      **DIM Columns**: Call ID, Agent, Date, Time, Topic
      **FACT columns**: Answer Y/N, Resolved, Speed of Answer, Avg Talk Duration, Satisfaction
      **Measures**: Answered Calls Rate, Abandoned Calls Rate, Resolved Calls Rate, Not-resolved Calls Rate, Average Satisfaction Score, Average Speed of Answer, Average Talk Duration, Min & Max Satisfaction Score, Target Satisfaction Score, Not resolved calls, Total Calls, Total Resolved Calls, Total Agents, Total Answered Calls, Time Range, SumOfSatisfactionScoreRating
  + Cleaning Data:
           Have null values in Speed of answer in seconds, Satisfaction rating. Replace null values with 0.
          Change the data type of Time column from Date/Time to Time only. 
         **Add new columns**: Customer Satisfaction Status, Answers Call, Abandoned Calls, Resolved Calls, Time Range
- **Step 2: Define point of view**
    + Forecast questions and needs from main stakeholders: 
      Agents' performance
      What is the current average satisfaction rate compared to the ideal satisfaction rate?
      What kind of issues/trends that customers most likely reach out to the support team? 
      Calls handled compared to total calls.
      The percentage of answered calls, abandoned calls, resolved calls, first contact resolution rate, etc
- **Step 3: Ideate**
    + Key metrics: Abandoned Calls Rate (First Call Resolution), Answered Calls Rate, Average CSAT Score, Average Talk Duration, Average Speed of Answer, Resolved Calls Rate, Not-resolved Calls Rate, Total Calls,       Total Agents,
    + Charts: Scorecards, Slicer, Clustered column chart, Line chart, Gauge, Clustered Bar Chart, Pie Chart, Stacked Area Chart
- **Step 4: Prototype**
    + 2 Dashboards: Customer Call Contact Overview, Agent Performance Analysis
    + Draft layout in papers: 
    **Customer Call Contact Overview**
    ![image](https://github.com/tammvu698/Customer-Call-Contact-Volume-Analysis---Power-BI-Dashboard/assets/67913407/7aadcc6c-5c12-4dbb-b80e-af97ef725e9e)
    
    **Agent Performance Analysis**
    ![image](https://github.com/tammvu698/Customer-Call-Contact-Volume-Analysis---Power-BI-Dashboard/assets/67913407/f9cf7f3a-adea-4b2c-9bdb-d5baaa6a9581)
    
    + Note: These are my first drafts for the layout of the dashboards, I actually modify the layouts more when I go through the dashboard in Power BI. 
- **Step 5: Review + Final results**
  ![image](https://github.com/tammvu698/Customer-Call-Contact-Volume-Analysis---Power-BI-Dashboard/assets/67913407/b1d65124-3752-4d11-8596-4701c9efe255)
  
  ![image](https://github.com/tammvu698/Customer-Call-Contact-Volume-Analysis---Power-BI-Dashboard/assets/67913407/36fa9d34-29a2-4aac-b014-1a53afa05bfb)


**Insights**

- We have a total of 5000 calls. 81% of the calls are answered and 73% of those problems from the calls are solved. 
- Abandoned Calls Rate: 19%. This means 19% of the calls are not picked up in the first calls or cannot reach onwards. Since this dataset does not mention the times the agent calls the customers, I will assume this rate is also the first call resolution rate. 
- The average CSAT score is 3.4 which is above average, however, it doesn’t reach the target CSAT score - 4.5. 
- Streaming is the issue that has the highest number of answered (847 calls) and resolved calls (749 calls). In reverse, technical support has the highest number of abandoned (214 calls) and not resolved calls (283 calls). 
- Top 3 topics with most calls: 
	+ Streaming  - 1022 calls
	+ Technical support - 1019 calls
	+ Payment related - 1007 calls
- Customers having Admin Support issues own the highest average CSAT score (3.43) 
- The customer care call team receives the most answered and resolved calls in January (1455 vs 1311 calls), then March (1301 vs 1174 calls), and the last with the least calls is February (1298 vs 1161 calls). 
- Jim is the agent who has the most calls (666 calls) with the highest number of answered calls (536 calls). However, Jim has the highest calls with a CSAT score in the range of 1 - 2 which is considered Not Satisfied status for customers. 
- Martha has the highest CSAT score which is 3.47 compared to Jim who has 3.39 - still an acceptable score. Martha owns the biggest total calls that have a score range from 4 - 5 which is considered as Satisfied calls for customers. 
- Joe has the lowest CSAT score which is 3.33 and is the second agent who has the lowest number of total calls (593 calls) - 
- Dan is the agent having the highest average talk duration (3.33 minutes)
- Joe has the longest average speed of answering customers (57.9 seconds). 




**Recommendation**
			
- Company Y should focus on improving the Streaming, Technical Support, and Payment-related issues. First priority should be Streaming, even though most of the cases from this issue are solved. 
- Joe should be working on improving his skills on how to make customers more satisfied since he has the lowest CSAT score out of 8 agents. 
- Dive deeper into collecting information regarding why the Customer Call team receives most of the calls in January 
