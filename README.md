# Web Scraping - Mission to Mars

## Background 

Mars is the fourth planet from the Sun and the second-smallest planet in the Solar System, being only larger than Mercury. In English, Mars carries the name of the Roman god of war and is often referred to as the "Red Planet".

In this Project, I build a web application that scrapes various websites for data related to the Mission to Mars and displayed the information in a single HTML page.


## Step 1 - Scraping

The initial scraping is conducted by using Jupyter Notebook, BeautifulSoup, Pandas, and Requests/Splinter, and a Jupyter Notebook file called [mssion_to_mars.ipynb](Missions_to_Mars/mssion_to_mars.ipynb) is used to complete all the scraping and analysis tasks.

### NASA Mars News

* I scraped the [NASA Mars News Site](https://redplanetscience.com/)and collected the latest News Title and Paragraph Text. The result looks as follows:


### Mars Space Images - Featured Image

* I Visited the url for Featured Space Image (https://spaceimages-mars.com/), and used splinter to navigate the site and find the image url for the current Featured Mars Image and assign the url string to a variable called `featured_image_url`.


### Mars Facts

* I Visited the Mars Facts webpage (https://galaxyfacts-mars.com/) and used Pandas to scrape the table containing facts about the planet including Diameter, Mass, etc and converted the data to a HTML table string.


### Mars Hemispheres

* I visited the USGS Astrogeology site (https://marshemispheres.com/), and  obtained high resolution images for each of Mar's hemispheres.

## Step 2 - MongoDB and Flask Application

I used MongoDB with Flask templating to create a new HTML page that displays all of the information that was scraped from the URLs. Then after, I converted the Jupyter notebook into a Python script with a function called `scrape` that will execute all of the scraping code from above and return one Python dictionary containing all of the scraped data.

* Next, I created a route called `/scrape` that will import the script and call `scrape` function.


