# Data-Analysis
Data Analyst in bay area, Analytics is exciting to me as it is the refinery to 21st century oil, Data, and I aim to combine the same with the rest of the skills in my toolbox. Here’s a skill snapshot - 
• Strong ability to comprehend and solve business problems
• Over 10 years of work experience (managed challenging projects)
• Analytical mindset/skills
• Comfort in using SQL, Python, Excel and Tableau
• Working knowledge of Descriptive and Inferential Statistics (Correlation, Regression etc.)
• Experienced in building dashboards
• Mechanical engineering background
• Understanding of data pipeline and familiarity with Machine Learning fundamentals
• First Principles Approach

https://github.com/grokab/Data-Science.git

Extracted csv data from X account
Loaded, cleaned and transformed data
Analyzed and visualized the data using Power Query
Create recommendations based on the analysis

# Social Media Growth Strategy Project for X account (user - Tom Mitchell)

## Executive Summary

Their content strategy balances **daily single posts (1-2)** with **weekly threads (3-5)**, ensuring a steady stream of updates while diving deeper into significant topics. However, October marked a pivotal moment with a **42% decline in total impressions**, highlighting the **need to reassess the approach to content and audience engagement dynamics**. Further analysis unveiled **threads as the engagement frontrunners**, boasting nearly double the interaction rates compared to single posts, and significantly outperforming in profile clicks and follower acquisition.

Moving forward, some recommendations **pivot on increasing thread-centric content from both a quantity and quality point of view as an immediate priority. **

## Project Overview

The aim of this project is to analyse X data to determine the best social media strategy for profile reach and growth. I’ll be looking specifically at which type of content - threads versus single posts - drives the most engagement from users on the platform. I’ll analyse posts' data to investigate the engagement rate of each post depending on its format and topic using Excel and Power Query. My objective is to understand the relationship between the type of post (single or thread) and the level of engagement it receives. It will then guide the social media content planning for better engagement. This project will provide the empirical evidence on which to base future social media strategies, thus putting the account in a stronger position to grow audience on X.

## Data Sources

For this project I will be using a CSV export of all of Tom's posts from 1st October 2023 – 31st October 2023. CSV files are a simple, widely accepted, and easy-to-understand data format. Being text files, they are human-readable and lightweight making them excellent for exporting small to medium datasets from platforms such as X. However, they have limitations. CSV files lack a standard schema, making interpretation of data more difficult across different systems. They also require manual export and can become inefficient with large amounts of data.

If the outcomes of my project proves significant, it might be worth considering the development of a data pipeline using X's API instead. This would also allow us to extract more data in real-time and potentially access more detailed data. The main benefits include scalability, ease of use and improved access to information which could open new doors for my data analysis and project potential.

## Data Cleaning & Transformation

I loaded the CSV file extracted from the X platform into Power Query. I formatted the headers on the data table for better comprehension and corrected the inferred data types to match the nature of information they hold, such as converting "X ID" and "impressions" into integers and "time" into datetime. Next, I removed any columns that were not needed for my analysis, such as "X id", "URL clicks", "hashtag clicks" and others related to promoted content. This makes my data model leaner and more manageable. From my X text, I excluded entries that contained "@" (replies to other X users) or "here:" (promotional posts), as they might have skewed the results.

The next challenge I faced was how to determine which posts were part of a thread and which were single posts. I decided to group posts by their posting date & time assuming that any post posted at the same day/time can be considered a thread and anything else can be considered a singular post. I duplicated the cleaned dataset and aggregated my data accordingly. Once I had validated the output, I merged that into my main dataset on the ‘post_text’ column. I renamed the additional column as 'number_of_posts'. I added a conditional column 'content_type' which was a thread or singular post flag. Through this process, I was able to eliminate irrelevant information and highlight the significant details of X data.

## Data Analysis

### 1. What is the current content strategy?
![Current_Content_Straetegy](https://github.com/grokab/Data-Science/assets/162400457/320a09bc-ac30-4000-9ca9-923da4f15bed)
The current content strategy revolves around a balanced approach, designed to engage the audience while maintaining consistency. On a daily basis, the account is publishing between **1-2 single posts**, ensuring that the audience receives regular updates and insights. This frequency allows the account to maintain a consistent presence and provide timely information. Additionally, to foster deeper discussions and dive into more comprehensive topics, they are crafting **3-5 threads each week**. These threads serve as platforms for more in-depth content, encouraging audience interaction and enhancing their brand's thought leadership in specific areas. By combining these two content formats, the account aims to cater to varying audience preferences, ensuring they deliver value consistently while encouraging meaningful engagement.

### 2. How do the impressions evolve over time?
![Comparison of Impressions](https://github.com/grokab/Data-Science/assets/162400457/6ddfdee3-6d39-4973-b9c7-6a6b0d815701)
Diving into the data, I spotted some interesting shifts in how often the content is seen. In October, there was a big drop—**impressions fell by 42%**. This is a clear signal. It tells us that potentially the audiences’ preferences are changing or the content quality has dropped. It also further validates the need for this project as, if nothing were to change, I believe this trend would continue and tarnish the reputation as a brand.

### 3. Which type of content (threads or single posts) generates the highest engagement rate?
![Engagement](https://github.com/grokab/Data-Science/assets/162400457/cad98301-7a68-4b2e-901c-ceb6574801a6)
When it comes to engaging the audience, **threads are clearly the winners**. They generate **double the engagement** compared to single posts. Specifically, threads have an engagement rate of 5%, while single posts lag behind at just 3%. So, in order to capture more attention and interaction from our audience, **focusing on threads will be more effective.**

### 4. Do impressions follow the same trend? Threads generate ~54% more Impressions vs Single Posts
![Impressions](https://github.com/grokab/Data-Science/assets/162400457/31515ff5-52d9-4a40-9bd2-69617d4059c2)
Looking at how many people see the content, **threads really stand out.** They get about **54% more views **than single posts do. To break it down, threads get 2.07 million views, while single posts only get 1.34 million. This shows that **threads are more effective in getting the content seen by a lot more people.**

### 5. Which type of content produces more user profile clicks and detail expands?

| Metric                     | Single Posts | Threads      | Verdict                                                |
|----------------------------|--------------|--------------|--------------------------------------------------------|
| Total User Profile Clicks   | 2745         | 3314         | |
| Total Detail Expands        | 6565         | 9389         | |


When it comes to getting people to click on our profiles and expand details, threads are the way to go. **Threads lead the pack,** getting **20% more profile clicks** than single posts. Specifically, single posts got 2,745 clicks, while threads scored 3,314. So, focusing on threads seems to be the smart move.

## Results/Findings

Moving forward, it's evident that thread posts are the driving force behind engagement and community growth, showcasing nearly double the engagement rates compared to single posts. Furthermore, they've demonstrated a remarkable ability to amplify reach, securing 54% more impressions and fostering an increase in clicks. Given these insights, **the immediate focus should be on enhancing the threads content strategy,** ensuring it remains robust and resonant with the audience's preferences.
