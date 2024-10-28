Webscrapper for Fellows Data

Overview
This Python script scrapes fellows' data from a multi-page website using Selenium. It captures information such as name, course, fellow ID, cohort, state of residence, and gender from each page and saves it into a CSV file.

Features
Automated Multi-Page Scraping: The script navigates through thousands of pages, capturing specific data fields for each fellow.
Headless Option: Enables headless mode for a more efficient and less resource-intensive scraping process.
Randomized Wait Times: Incorporates randomized delays to reduce the chance of being detected as a bot.


Prerequisites
Python 3.x - Ensure Python is installed and updated on your system.
Chrome WebDriver Manager - webdriver_manager is used to manage ChromeDriver installations.
Selenium - Selenium automates browser actions.
Install required libraries with:

pip install selenium webdriver-manager

Script Details

Dependencies
Selenium: To automate the browser interaction.
webdriver-manager: Automatically installs the latest version of ChromeDriver.

Scraping Steps
The script navigates to the initial page of the fellows' directory.
For each page:
It waits until the table data is loaded.
Scrapes each fellow’s details from the table.
Clicks the “Next” button to proceed to the following page.
A randomized delay between pages reduces the risk of being blocked.

Data Captured
Name, Course, Fellow ID, Cohort, State of Residence, Gender

Output
The data is saved in a CSV file called fellows_data_test.csv.


Usage Instructions

Set Up Chrome Options:
Uncomment the line in the code to enable headless mode if you don’t need a visible browser.

Run the Script:
python your_script_name.py

Adjust Page Range:
Change the range value in for page_number in range(1, 3230): to specify the number of pages you want to scrape.

CSV Output
Data is saved in a CSV file named fellows_data_test.csv in the following format:

Name	Course	Fellow ID	Cohort	State of Residence	Gender

Error Handling
The script includes exception handling for each page and row. If an element is not found, or if a page fails to load, it prints an error message and attempts to proceed.


