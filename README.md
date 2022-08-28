# chronicle-job-advertisement-scraper

Scrapes job information from listings on The Chronicle of Higher Education -> **[Link](https://jobs.chronicle.com/jobs/faculty-positions/north-america/tenured-tenured-track/)**.

## Description
 - Data is stored in `./data` 
 - Data scraping is performed by the notebook `the-chronicles-of-higher-ed-scraper.ipynb`
 - Data validation and recovery is performed by the notebook `validate-existing-data.ipynb`

The following information is scraped:

 - Unique Id of the Job Listing on the Chronicle website.
 - Job title
 - URL to the job listing.
 - Whether the listing is for a diversity related job
 - Employer
 - Location 
 - Salary
 - The date the job was posted
 - Job description.
 - Type of position

All of this information is publicly avaliable through the Chronicle of Higher Education website.


## Why Data is Needed

This is being used for a project in Princeton's SSP lab analyzing diversity in jobs.


## Implementation Details

The code written in `the-chronicles-of-higher-ed-scraper.ipynb` is a few years old and was written 
by someone no longer doing research in the lab. The code attempts to scrape information from the 
Chronicle website by parsing the HTML dom using a variety of selectors. It removes duplicates from the 
scraped jobs by comparing what jobs are currently avaliable with what jobs were already scraped in the 
batch of data. It's not future proof, and might need modification in the future. If another researcher 
comes across this in the future needing to understand/rewrite this code, it would be best to use the
information encoded into the page by Google Tag Manager.

