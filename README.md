# Scraper

For scraping, we use the Selenium package:

#### Webdriver setup - Selenium

[Selenium](http://selenium-python.readthedocs.io) uses a webdriver to navigate websites.

Run these commands in PowerShell to download the chrome webdriver programmatically:

```PowerShell
cd C:\codebase\github\HQYDataScienceClub\AppSentiment
$url = "https://chromedriver.storage.googleapis.com/2.38/chromedriver_win32.zip"
Invoke-WebRequest -Uri $url -OutFile ".\env\chromedriver_win32.zip"
Expand-Archive -Path ".\env\chromedriver_win32.zip" -DestinationPath .\env\
Remove-Item .\env\chromedriver_win32.zip
```

Alternately, download manually from [sites.google.com/a/chromium.org](https://sites.google.com/a/chromium.org/chromedriver/) and save under the `env` directory:

```
Curiation
    ├─ docs
    ├─ env
    |   ├─ venv
    |   └─ chromedriver  <–– save chrome webdriver here
    ├─ src
    |   └─ Motivosity.py
    └── README.md
```

#### Environment Setup - venv


```PowerShell
python -m venv env/venv
. .\env\venv\scripts\activate.ps1
python -m pip install --upgrade pip
pip install selenium pandas
deactivate
```


