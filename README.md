# Web-Scraping-Challenge
As a part of this project, a web application was built that scrapes various websites for data related to the Mission to Mars and displays the information in a single HTML page using Flask.  
![alt text](https://github.com/fbrowther/Web-Scraping-Challenge/blob/main/Flask%20images/cropped%20flask%20image%20for%20readme.png)

## Technologies used in the project:
    (1) Beautiful Soup & Splinter: To scrape data from various websites.
    (2) Flask: To build the web application.
    (3) HTML & Bootstrap (CSS): To design and style the webpage.
    (4) PyMongo: To interacte with the MongoDB to store scraped data and retrieve to display on the webpage.
    (5) Pandas: To design the Mars v. Earth comparison table for webpage.

## Part1: Web Scraping

The HTML pages of the websites that needed scraping were inspected and necessary information was gathered to write the codes. Scraping was carried out using Jupyter Notebook, BeautifulSoup, Pandas, and Requests/Splinter.

### (1) NASA Mars News Feed -

For the NASA Mars News feed "https://redplanetscience.com" was set up to be visited and the latest News Title and Paragraph Text was scrapped. This information was assigned to a variable to refer to them later. 

### (2) Featured Space Image of Mars -

The URL for the Featured Space Image site "https://spaceimages-mars.com/" was visited and the image URL to the full-sized .jpg image was identified.
The image URL for (the curren Featured) Mars Image was built before assigning it to the URL string of a variable called featured_image_url. 

### (3) Mars Facts -

In order to obtain the facts about Mars, "https://galaxyfacts-mars.com/" was visited and the table containing facts about the red planet including diameter, mass, moon, temperature etc were scraped using pandas. The table was then converted to a HTML table string and stored in the same dictionary as above.

### (4) Mars Hemispheres -

Mars astrogeology site ("https://marshemispheres.com/") was visited to obtain high-resolution images for each hemispheres of Mars. Image URL string for the full resolution hemisphere image and the hemisphere title containing the hemisphere name was created for each hemisphere and a Python dictionary was created to store the data using the keys img_url and title.


## Part2: MongoDB

After scraping all the required information for the HTML page, a database in MongoDB (mission_to_mars) was created, to store the scraped data from the URLs above. This data will be updated as one clicks 'Get Latest Mars Data' button on the final html webpage. Update of the mongoDB collection was confirmed with updated information everytime an update was evident on the webpage by clicking 'Get Latest Mars Data' button as follows-

![alt text](https://github.com/fbrowther/Web-Scraping-Challenge/blob/main/Flask%20images/Screenshot%202022-12-06%20at%2011.43.35.png)


## Part3: Flask Application

Jupyter notebook containing  all the codes were used to create a scrape_mars.py file using python function scrape(). This function executed all the scraping code from above and returned one Python dictionary containing all the scraped data. This updated dictionary was stored in MongoDB. 

Flask establishes connection with the MongoDB database (mission_to_mars) and passes the latest Mars data into an HTML template for displaying in the appropriate HTML elements. 


## Part4: HTML Webpage displaying the most recent Mars Data (as of 06/12/2022)
The screenshot of the updated HTML page has been included confirming its successful deployement.

![alt text](https://github.com/fbrowther/Web-Scraping-Challenge/blob/main/Flask%20images/Screenshot%202022-12-06%20at%2011.43.57.png)


## Important Note: 
Please click 'Get Latest Mars Data' button on the html webpage to update webpage with more recent data.



