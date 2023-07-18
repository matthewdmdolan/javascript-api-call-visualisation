# Javascript Web Scraper - MVP 

I am starting a project at work in which web scraping is necessary to accquire some data for pipelines. In the process of trying to find the best method, I've found that all have significant trade offs. Ultimately, a lot of the discussions I saw after researching, were centred around Python (my preferred language). Out of the Python options, scrapysplash has been  my favourite, in terms of its ability to efficiently deal with javascript content and offers a great testing framework.

However, the fact it needs a container to run the Splash API is likely to be an issue (public sector). Therefore, I had an idea that it may be quicker to use the technology which is the downfall of most of the options below. I'd already used javascript in web applications for other projects, so I thought I would build upon that and to try and test how that would work. It's likely going to require Python for the data cleaning due to javascript's limited abilities in this respect, therefore there is a chance I will have to use the APEX js package to call a python script for data cleaning. However, this is likely to be the quickest option.


# Web Scraping Packages 101 :

(excerpt from a very rough WIP medium article)

'HTTP Request' packages:
can't deal with javascript and doesn't have anywhere near the debugging capabilites of scrapy

1. Scrapy
+ brilliant framework that is a joy to work with and has some great debugging abilities
- cannot work with javascript heavy websites out the box

Caveat: Scrapy documentation suggests we can use the network tool of your web browser to see how your web browser performs the desired request, and try to reverse engineer that request with Scrapy (source: Scrapy.https://docs.scrapy.org/en/latest/topics/dynamic-content.html). However, this is required for every request and becomes incredibly inefficient.
  
2. html_requests
+ Allows for easy web scraping using fluid syntax with low technical barriers to entry
- Render feature very inconsistent

3. beautifulsoup
+ Low code meaning great for beginners
+ Good parsing functionality 
- very limited functionality
- very slow with large datasets

  
"headless browser" packages:
Packages whereby a real web browser fetch and render the website for you. In essence, it allows you to scrape information from dynamic websites, that rely on javascript.

1. Selenium (Python):
+ great functionality and comfortably deals with websites that are heavy on javascript
- incredibly slow: unlikely to provide the data volumes necessary to provide meaningful pipelines

caveat: there have been discussions of using distributed computing methods to help with this, but this project is within a public sector organisation where resources are limited. Therefore, not an option for this case but it makes for an interested reading nevertheless https://medium.com/@kevanahlquist/selenium-grid-cluster-example-with-docker-and-fig-24943a5eca42

2. ScrapySplash (Python):
+ makes working with javascript a breeze and offers some great testing in terms of allowing pages to be rendered in a gui and also via a shel
+ Utilises the brilliant Scrapy framework 
+ mMch quicker than selenium
- requires a container in order to host the Splash API which could be an issue in these circumstances due to having to use windows and being a public sector org

3. Playwright (multi language):
+ offers multi-language support

4. Puppeteer (JS):
+ extremely quick
- clunky data cleaning compared to python
  

