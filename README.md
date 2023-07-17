# Javascript API Call Visualisation 

I am starting a new work project in which data scraping is required to accquire some data for pipelines, and in the process of trying to find the best method I've found all have significant trade offs. 

1. Selenium:
+ great functionality and comfortably deals with websites that are heavy on javascript
- incredibly slow and unlikely to be able to provide enough data to make meaningful analysis

caveat: there have been discussions of using distributed computing methods to help with this, but this project is within a public sector organisation, but it makes for interested reading https://medium.com/@kevanahlquist/selenium-grid-cluster-example-with-docker-and-fig-24943a5eca42

2. Scrapy
+ brilliant framework that is a joy to work with and has some great debugging abilities
- cannot work with javascript websites out the box

3. ScrapySplash
+ makes working with javascript a breeze and offers some great testing in terms of allowing pages to be rendered in a gui and also via a shell  
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
