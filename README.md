#Aviation Accident Statistics

Topic: Aviation Accident Statistics
 

Main Source of data

https://aviation-safety.net/statistics/

sub-sources

-	Statistics by Period

Fatal accidents and fatalities per year for airliner (14+ passengers) hull-loss accidents
Fatal accidents and fatalities per year for corporate jet hull-loss accidents
Hijackings and hijacking per year
All figures are excl—ground fatalities.	

-	100 Worst aviation accidents (including ground fatalities)

List of the 100 worst aviation occurrences (including criminal occurrences), including ground fatalities, including collision fatalities

-	Worst geographical regions

List of the 25 geographical regions having the highest number of fatal civil airliner accidents from 1945 until now. Military accidents, corporate jets, hijackings (and other criminal occurrences) are not included.



The following activities are done to achieve our desired results the following procedures needed to be performed


Web scraping

https://www.ntsb.gov/investigations/AccidentReports/Pages/aviation.aspx
https://aviation-safety.net/database/

Our initial data was scraped, but because of inconsistencies in the dataset, it was abandoned and a new dataset was identified to fulfil out teams goal.

Current data set:
https://aviation-safety.net/statistics/

the team moved forward in scraping the data using cleaned and exported as a csv file using Jupyter notebook. 

The next phase was to choose a database

-	MongoDB was chosen because of its status as a document database and inherent flexibility.

-	From there, each member of our team ran the MongoDB code to create the same local database. This process gave us quick and easy access to the data for visualization purposes.

From there we made use of a flask app to render the MongoDB data as json. This made it easy for D3 to use our Mongo data for the visualizations.

The visualization libraries we made use of are listed below

-	Leaflet JS

https://leafletjs.com

-	Chart JS

https://www.chartjs.org

-	Plotly

https://plotly.com

With these libraries we were able to create the following visualizations for the datasets listed above

* Statistics by Period
   * A bar graph that shows the number of incidents per year over a 77-year time period.

* Worst geographical regions: 
   * A scatter plot that shows the number of accidents per country.
   * A bar graph that shows the number of accidents per country.
   * A leaflet map that conveys the amount of accidents per country through increased or decreased marker size.

* 100 Worst aviation accidents (including ground fatalities)
   * A bar graph displaying 100 worst accidents by continent.
