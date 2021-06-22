# undetectable-scrapy-selenium
This merges scrapy_selenium (https://github.com/clemfromspace/scrapy-selenium) middleware with undetected_chromedriver (https://github.com/ultrafunkamsterdam/undetected-chromedriver) to provide an undetectable chromedriver within the scrapy_selenium middleware.

Add the SeleniumUcMiddleware to the downloader middlewares in settings.py: 
DOWNLOADER_MIDDLEWARES = {
# The priority of 560 is important, because we want this middleware to kick in just before the scrapy built-in `RetryMiddleware`.
    'scrapy_selenium_ud.middlewares.SeleniumUcMiddleware': 800
}
