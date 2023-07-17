# Javascript API Call Visualisation 

I am starting a project at work in which web scraping is necessary to accquire some data for pipelines. In the process of trying to find the best method, I've found that all have significant trade offs (as with everything in life). Ultimately, a lot of the discussions I saw after researching, were centred around Python (my preferred language). However, I had an idea that it may be quicker to use the technology which is the downfall of most of the options below. I'd already used javascript in web applications for other projects, so I thought I would build upon that and to try and test how that would work. 

It's likely going to require Python for the data cleaning due to javascript's limited abilities in this respect, therefore 

This repo is simply just to work with some of the data viz packages prior to working on an end to end web scraping project in JS.

1. Selenium:
+ great functionality and comfortably deals with websites that are heavy on javascript
- incredibly slow and unlikely to be able to provide enough data to make meaningful analysis

caveat: there have been discussions of using distributed computing methods to help with this, but this project is within a public sector organisation where resources are limited. Therefore, not an option for this case but it makes for an interested reading nevertheless https://medium.com/@kevanahlquist/selenium-grid-cluster-example-with-docker-and-fig-24943a5eca42

2. Scrapy
+ brilliant framework that is a joy to work with and has some great debugging abilities
- cannot work with javascript websites out the box

3. ScrapySplash
+ makes working with javascript a breeze and offers some great testing in terms of allowing pages to be rendered in a gui and also via a shell
+ much quicker than selenium
- requires a container in order to host the Splash API which could be an issue in these circumstances due to having to use windows and being a public sector org

4. html_requests
+ Allows for easy web scraping using fluid syntax with low technical barriers to entry
- I found the render feature very inconsistent

5. beautifulsoup
+ low code
- very limited functionality: can't deal with javascript and doesn't have anywhere near the debugging capabilites of scrapy

6. Playwright
TBC


So far scrapysplash has been far and away my favourite in terms of functionality and speed. 
