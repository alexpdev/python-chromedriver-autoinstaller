# pychromedriver
Download [chromedriver](https://chromedriver.chromium.org/) for the currently installed version of chrome. 

## Installation

```bash
pip install pychromedriver
```

## Usage

When install is called it downloads the correct version of chromedriver and adds it to the sys.path.

```python
from selenium import webdriver
from pychromedriver import ChromeInstaller

ChromeInstaller.install()

driver = webdriver.Chrome()
```

Calling install will also return the the path to the downloaded binary.

```
from selenium import webdriver
from selenium.webdriver.chrome.service import Service as ChromeService
from pychromedriver import ChromeInstaller

path_to_chromedriver_binary = ChromeInstaller.install()

service = ChromeService(path_to_chromedriver_binary)

driver = webdriver.Chrome()
```
