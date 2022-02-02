# Open-Miami-Street-Map-Data

Project Overview
You will choose any area of the world in https://www.openstreetmap.org and use data munging techniques, such as assessing the quality of the data for validity, accuracy, completeness, consistency and uniformity, to clean the OpenStreetMap data for a part of the world that you care about. Finally, you will choose either MongoDB or SQL as the data schema to complete your project.

What will I learn?

After completing the project, you will be able to:
•	Assess the quality of the data for validity, accuracy, completeness, consistency and uniformity.
•	Parse and gather data from popular file formats such as .csv, .json, .xml, and .html
•	Process data from multiple files or very large files that can be cleaned programmatically.
•	Learn how to store, query, and aggregate data using MongoDB or SQL.

Why this Project?

What’s so hard about retrieving data from databases or various files formats? You grab some data from this file and that database, clean it up, merge it, and then feed it into your state of the art, deep learning algorithm … Right? 
But the reality is this -- anyone who has worked with data extensively knows it is an absolute nightmare to get data from different data sources to play well with each other. 
And this project will teach you all of the skills you need to deal with even the most nightmarish data wrangling scenarios. 

Why is this Important to my Career?

The skills in this project are some of the most important for your career. Any data analyst will need to wrangle data before they can do any analysis. At Udacity, how would we know when students submit projects unless we made sure to report the timestamp? How would we be able to compare that to when students finish watching videos unless we built data pipelines to get all of this information in one place? Data analysts help with collecting and cleaning the data, or what is often called "data wrangling."
Data analysts and data scientists can spend 50%-80% of their time data wrangling. A huge benefit of this is that collecting and cleaning data means you will know the data very well, and be better prepared to analyze it.

To Prepare for the Project

Step 1: Complete the Data Wrangling Course.
Step 2: Choose between MongoDB and SQL and complete the associated course 
For MongoDB, prepare for this project with: MongoDB For Data Analysis. (If this link does not work, you can find the MongoDB content in the Extracurricular section of the Nanodegree materials.)
For SQL, prepare for this project with: SQL for Data Analysis.
Note
If you have successfully completed the project for the Data Wrangling with MongoDB course in the past (which entails having graduated from the course and having access to your course certificate), simply email us at dataanalyst-project@udacity.com with your passing evaluation and we'll give you credit for this project.


Project Details

This project is connected to the Data Wrangling course. You have the choice between two databases for this project: SQL and MongoDB. For an explanation of the differences between these two databases, continue to the next concept in this lesson. There are separate instructions where relevant below for each database choice.

Here's what you should do:

Step One - Complete Programming Exercises
Make sure all programming exercises are solved correctly in the "Case Study: OpenStreetMap Data" Lesson in the course you have chosen (MongoDB or SQL). This is the last lesson in that section.

Step Two - Review the Rubric and Sample Project
The Project Rubric will be used to evaluate your project. It will need to Meet Specifications for all the criteria listed. Here is an example of what your final report could look like if you choose the SQL option:
SQL Sample Project

Step Three - Choose Your Map Area
Choose any area of the world from https://www.openstreetmap.org, and download a XML OSM dataset. The dataset should be at least 50MB in size (uncompressed). We recommend using one of the following methods to download a dataset:
•	Use the Overpass API to download a custom square area. Explanation of the syntax can found in the wiki. In general you will want to use the following query:(node(minimum_latitude, minimum_longitude, maximum_latitude, maximum_longitude);<;);out meta; e.g. (node(51.249,7.148,51.251,7.152);<;);out meta; the meta option is included so the elements contain timestamp and user information.
•	You can use the Open Street Map Export Tool to find the coordinates of your bounding box. Note: You may not be able to use the Export Tool to actually download the data, the area required for this project is too large. After selecting a region, you can try clicking the Overpass_API link down the tool bar to perform the export and download.

Step Four - Process your Dataset
It is recommended that you start with the problem sets in your chosen course and modify them to suit your chosen data set. As you unravel the data, take note of problems encountered along the way as well as issues with the dataset. You are going to need these when you write your project report.
SQL
Thoroughly audit and clean your dataset, converting it from XML to CSV format. Then import the cleaned .csv files into a SQL database using this schema or a custom schema of your choice.
MongoDB
Thoroughly audit and clean your dataset, converting it from XML to JSON format. Then import the cleaned .json file into a MongoDB database.
Hints and Tips
•	Feel free to adapt the code from the Case Study lesson to help you approach the auditing of your data. It will help your organization by creating a new script for each aspect of your dataset that you audit. Each field that you audit should also include a function that will help you update your dataset.
•	You may want to start out by looking at a smaller sample of your region first when auditing it to make it easier to iterate on your investigation. See code in the notes below for how to do this. You can use a small (1-10MB) sample to make sure that your code works, and then an intermediate sample to check for the most common problems to clean.
•	Remember to perform data cleaning when you convert the XML into CSV or JSON format. You won't change the original data file, only the data that you plan on inserting into your database. This is where your earlier organization will pay off, since you can just import the update functions from your auditing scripts into the cleaning and conversion script.

Step Five - Explore your Database
After building your local database you’ll explore your data by running queries. Make sure to document these queries and their results in the submission document described below. See the Project Rubric for more information about query expectations.

Step Six - Document your Work
Create a document (pdf, html) that directly addresses the following sections from the Project Rubric.
•	Problems encountered in your map
•	Overview of the Data
•	Other ideas about the datasets
Try to include snippets of code and problematic tags (see  SQL Sample Project) and visualizations in your report if they are applicable.
Use the following code to take a systematic sample of elements from your original OSM region. Try changing the value of k so that your resulting SAMPLE_FILE ends up at different sizes. When starting out, try using a larger k, then move on to an intermediate k before processing your whole dataset.

