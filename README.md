## FIFA Player Scouting and Transfer Dashboard

<img width="1920" height="1080" alt="FIFA_Dashboard" src="https://github.com/user-attachments/assets/533d2518-4b8b-452b-a887-5a56eb5f5e9a" />

# Project Overview
Welcome to my FIFA Player Scouting and Transfer Dashboard! I designed this interactive project specifically for football team managers and scouts. The goal is to make it easier to track expiring player contracts, pinpoint transfer targets based on tactical needs, and analyze different play styles across top-tier clubs.

This was an end-to-end data project where I used Python to handle the heavy lifting of data cleaning and feature engineering, and Power BI to bring the insights to life visually.

(Note: replace this link with your uploaded image file)

# Key Features and Business Value
Contract Monitoring: Users can quickly spot players with expiring contracts, which is crucial for planning free transfers and early negotiations.

Targeted Scouting: I included dynamic slicers so users can easily filter the database by pitch position, nationality, and preferred foot to find exactly who they need.

Top Club Analysis: A dynamic Tree Map automatically filters to display the top 10 clubs based on their overall player ratings.

Play Style Profiling: I embedded a custom Python radar chart directly into Power BI. It takes 17 underlying player statistics and visually maps out their core attributes, categorizing them into archetypes like Speedster, Playmaker, or Finisher.

# Tools and Technologies
Data Cleaning and Scripting: Python (using Pandas, NumPy, and UnicodeData)

Visualizations: Power BI and Matplotlib (for the custom radar chart)

Key Techniques: Feature engineering, text normalization, regular expressions (regex) for data extraction, and bivariate analysis.

Behind the Scenes: The Data Cleaning Process
Real-world data is rarely ready to chart right out of the box. Before building the dashboard, I wrote a Python script (available in scripts/data_cleaning.py) to clean and structure the raw dataset. Here is a quick look at what that involved:

Financial Normalization: I converted messy, string-based currency values (like '€110.5M' or '€565K') into clean, usable numeric floats so they could be graphed accurately.

Text Normalization: To make sure the Power BI slicers worked perfectly without search errors, I stripped out complex accents and special characters from club and player names (for example, standardizing Atlético Madrid to Atletico Madrid).

Date Extraction: I used regex to pull clean, 4-digit years out of mixed-format contract end dates.

Feature Engineering: I created a brand-new "Play Style" metric. By grouping 17 individual attributes into six major archetypes (Speedster, Playmaker, Finisher, Dribbler, Ball Winner, and Physical/Tank), the script calculates the highest average to dynamically assign a distinct play style to every single player.

# How to Run This Project
Download the .pbix file located in the dashboard/ folder.

Open the file using Power BI Desktop.

A quick note: Because I used a custom Python visual for the radar chart, you will need to have Python installed on your computer and enabled in your Power BI global scripting settings for that specific chart to render correctly.
