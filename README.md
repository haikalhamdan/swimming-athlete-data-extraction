🏊‍♀️ Diving Data Extraction — Women’s 3m Springboard (Final Round)
📖 Overview

This project extracts structured diving results data from the World Aquatics competition website for the Women’s 3m Springboard Final Round, focusing on Michelle HEIMBERG and Grace REID.

The goal was to automate data collection of detailed performance metrics such as dive descriptions, degrees of difficulty, judges’ scores, and total points — and export them into a structured CSV file for analysis.

🌐 Data Source

Competition Page:
https://www.worldaquatics.com/competitions/4864/67th-international-divers-day/results?event=ac05a075-5a4e-420a-8b4d-91c965cf47d9

🧰 Tools and Libraries

Implemented in Python using the following packages:

pip install selenium pandas

Imports Used
from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import pandas as pd
import time


Purpose of Each Library:

selenium — Automates browser actions and extracts dynamic webpage content

pandas — Structures the extracted data and exports to CSV

time — Manages small delays during automated interactions

⚙️ Process Summary

Launch Chrome WebDriver using Selenium.

Navigate to the target competition page.

Locate and expand result sections for:

Michelle HEIMBERG

Grace REID

Extract:

Dive number and description

Degree of difficulty

Individual judges’ scores

Dive points and cumulative total

Save the structured results into diving_results.csv using pandas.

📊 Sample Output (diving_results.csv)
Athlete	Dive Number	Dive Description	DD (Degree of Difficulty)	Judge 1	Judge 2	Judge 3	Judge 4	Judge 5	Judge 6	Judge 7	Dive Points	Total Points
Michelle HEIMBERG	1	405B - Inward 2.5 Somersaults, Pike	3.0	4.5	4.0	4.5	4.5	4.5	4.5	4.5	40.5	40.5
Michelle HEIMBERG	2	107B - Forward 3.5 Somersaults, Pike	3.1	7.0	7.0	6.5	6.5	6.5	6.5	6.5	60.45	100.95
Grace REID	1	405B - Inward 2.5 Somersaults, Pike	3.0	6.0	6.0	6.0	6.0	6.0	6.0	6.0	55.5	55.5
Grace REID	2	107B - Forward 3.5 Somersaults, Pike	3.1	6.5	6.5	6.5	6.5	6.5	6.5	6.5	55.8	111.3

(only a few rows shown as example)

💡 Highlights

Automated extraction from a dynamic sports result page

Combined main and sub-table elements into a single dataset

Exported structured, analysis-ready results

Demonstrated use of Selenium waits for reliable scraping
