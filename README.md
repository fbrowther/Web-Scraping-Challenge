# Web-Scraping-Challenge

For this project,  it was required to build a web application that scrapes various websites for data related to the Mission to Mars and displays the information in a single HTML page using Flask. 

## Part1: Web Scraping 

The HTML pages of the webpages that needed scraping were inspected to gather information write the necessary codes. Scraping was carried out using Jupyter Notebook, BeautifulSoup, Pandas, and Requests/Splinter.

### (1) NASA Mars News Feed

For the NASA Mars News feed "https://mars.nasa.gov/news/" was set up to be visited and the latest News Title and Paragraph Text was scraped. This information was assigned a variable name to refer to later. 

### (2) Featured Space Image of Mars

The URL for the Featured Space Image site "https://spaceimages-mars.com/" was visited and the image URL to the full-sized .jpg image was identified.
The image URL for (the curren Featured) Mars Image was built before assigning it to the URL string of a variable called featured_image_url. 

### (3) Mars Facts

In order to obtain the facts about Mars "https://galaxyfacts-mars.com/" was visited and the table containing facts about the red planet including diameter, mass, moon, temperature etc were scraped using pandas. The table was then converted to a HTML table string.

### (4) Mars Hemispheres

Mars astrogeology site ("https://marshemispheres.com/") was visited to obtain high-resolution images for each hemispheres of Mars. Image URL string for the full resolution hemisphere image and the hemisphere title containing the hemisphere name was created for each hemisphere and a Python dictionary was created to store the data using the keys img_url and title.


![alt text](https://github.com/fbrowther/Web-Scraping-Challenge/blob/main/Deployed%20Webscraping%20App%20Page.png)


## Part2: MongoDB and Flask Application
After scraping all the required information for the HTML page, a database was created in MongoDB (mission_to_mars) to store the scraped data from the URLs above. This data will be updated constantly as we click 


Part 2: MongoDB and Flask Application
Use MongoDB with Flask templating to create a new HTML page that displays all the information that was scraped from the URLs above.


Start by converting your Jupyter notebook into a Python script called scrape_mars.py by using a function called scrape. This function should  execute all your scraping code from above and return one Python dictionary containing all the scraped data.


Next, create a route called /scrape that will import your scrape_mars.py script and call your scrape function.

Store the return value in Mongo as a Python dictionary.



Create a root route / that will query your Mongo database and pass the Mars data into an HTML template for displaying the data.


Create a template HTML file called index.html that will take the Mars data dictionary and display all the data in the appropriate HTML elements. Use the following as a guide for what the final product should look like, but feel free to create your own design.


