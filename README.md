# JOB OPPORTUNITIES IN THE US REPORT - USF HANDSHAKE

The project aims to visualize the work opportunities in the US based on the job openings on USF Handshake.

## STEP-BY-STEP PROCESS
### Web Scrapping
1. Go to the location of Google Chrome application and run the cmd. Then paste this line of code:
```bash
chrome.exe --remote-debugging-port=8000 --user-data-dir="D:\Chromedata"
```
2. In the new Google Chrome window, log in to USF Handshake and open [Job Postings](https://app.joinhandshake.com/stu/postings).
3. Use [handshake_scrapping.ipynb](https://github.com/Scarlett04/handshake-scrapping/blob/main/handshake_scrapping.ipynb) to scrape the website. 
#### NOTE: In order to avoid errors caused by a poor Internet connection, it is recommended to perform multiple scraping attempts and concat the resulting files.

### Data Cleaning
1. Use [data_cleaning.ipynb](https://github.com/Scarlett04/handshake-scrapping/blob/main/data_cleaning.ipynb) to explore and clean the data. Feel free to make any necessary adjustments to ensure that you have a clear understanding of your data.
2. To get the locations and states abbreviations of each job title, run [data_explode.ipynb](https://github.com/Scarlett04/handshake-scrapping/blob/main/data_explode.ipynb).
#### NOTE: Some CSV files may contain formatting errors that affect the next step. Consider saving the file as .xlsx or any other more stable types.

### Data Visualization
1. Install Tableau through this link: https://www.tableau.com/.
2. Create a new Workbook using 3 files: 
- Job Information Data: [csv](https://github.com/Scarlett04/handshake-scrapping/blob/main/csv/modified_data.csv) / [xlsx](https://github.com/Scarlett04/handshake-scrapping/blob/main/Excel/modified_data_final.xlsx).
- Location Data: [csv](https://github.com/Scarlett04/handshake-scrapping/blob/main/csv/location.csv) / [xlsx](https://github.com/Scarlett04/handshake-scrapping/blob/main/Excel/location.xlsx).
- Hexagon Map Coordinators: [csv](https://github.com/Scarlett04/handshake-scrapping/blob/main/csv/hexmap_plots.csv) / [xlsx](https://github.com/Scarlett04/handshake-scrapping/blob/main/Excel/hexmap_plots.xlsx).
3. Establish the relationship between 3 files: First, the Job Information Data is linked with Location Data by ID. The Location Data's "States abbreviation" is equivalent to Hexagon Map's "Abbreviation".
4. Feel free to use any charts to visualize your data. Here is an example dashboard: [Data Visualization.twbx](https://github.com/Scarlett04/handshake-scrapping/blob/main/Data%20Visualization.twbx).

![Data Visualization](https://user-images.githubusercontent.com/86146191/229308746-80ef2683-06d9-4375-a941-200564ab9185.jpg)

Video Demo:

https://user-images.githubusercontent.com/86146191/227438199-2f0fdeb7-617c-4fa0-86f4-6cbda141c29b.mp4

Tableau: https://public.tableau.com/app/profile/tran.ho4576/viz/DataVisualization_16803730460700/Dashboard1
