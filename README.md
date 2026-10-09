# UK Planning Portal Scrapers

Python and Selenium scripts that collect planning applications from UK local council planning portals. Each script searches the portal across a date range, opens every application, saves its details as text files and downloads its documents into a tidy folder per application.

## Supported portals

| Council | Portal | Script |
|---|---|---|
| Adur and Worthing | planning.adur-worthing.gov.uk | adur_worthing_scraper.py |
| Babergh and Mid Suffolk | planning.baberghmidsuffolk.gov.uk | babergh_mid_suffolk_scraper.py |
| Barnet | publicaccess.barnet.gov.uk | barnet_scraper.py |

## What each script does

1. Opens the council's advanced search and walks through the chosen date range.
2. For every application, saves the summary, further information and other detail tabs as text files.
3. Downloads the application documents, waits for each download to finish and extracts zip or rar archives.
4. Writes a timestamped log of every step.

Monitor.py watches the running scraper processes and restarts any that stop, so long runs can be left unattended.

## Setup

```
py -m pip install selenium webdriver-manager python-dateutil patool rarfile pyzipper psutil selenium-stealth
```

Microsoft Edge must be installed. Python install.txt lists the full setup steps.

## Author

Sourab Kumar Saha, data analyst and automation developer. Available for scraping and automation work on [Fiverr](https://www.fiverr.com/spontaneoussrv).
