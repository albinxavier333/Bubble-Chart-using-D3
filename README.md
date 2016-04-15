# Bubble-Chart-using-D3
D3 visualisation of mobile subscription and telephone subscription of 10 country

Visualisation for Mobile Cellular Subscription v/s Fixed Telephone
Subscription from 2000 to 2015 using D3.js
1.Introduction
Visualisation of a dataset is a sensible and highly persuasive way of communication. It helps to
understand the data in hand in a much better way. Even though how complex the data is; visualisation make
the interpretation of data much simpler. The key benefit of visualisation is better understandability,
readability, simplicity.
In this visualisation we are using D3.js to visualise the data. We are comparing Mobile cellular
subscription and Fixed Telephone subscription between ten countries over the years of 2000 to 2015. The
chart which is used to visualise the data over a span of 15 years is the time series motion chart [1].
2. Dataset
The data is collected from the http://data.worldbank.org/ [2] where the country wise data is
downloaded. We will be considering 11 datasets from the world bank website. The countries which are
considered when visualising the data is India, Ireland, United States, Australia, China, Japan, UK, France,
Brazil and South Africa. The dataset will be having a lot of unwanted data which will not be taken into
consideration when doing the visualisation, this data will be filtered out, and only the data which we need
for the visualisation will be retained in the csv file. As all the countries data are in different csv files, the
data will be merged into one file for visualisation. Dataset containing the population of the above said
counties are also downloaded into the system which will be used as a segment of the visualisation activity.
The population will determine the size of the dot which will be visualised in the motion chart. The bigger
the population of a country, bigger will be the size of the dot which is getting displayed in the visualisation.
3. Process
3.1 Importing the Dataset
11 different datasets are used in this visualization. Ten datasets are of different countries (India,
Ireland, United States, Australia, China, Japan, UK, France, Brazil and South Africa) which will get
displayed in the motion chart. The 11th one will be the dataset which contains the population of the different
countries which is getting displayed in the visualisation.
Steps to download the country wise data:
• Log in to the website http://data.worldbank.org/
• Click on the link ‘By Country’ in the home page.
• Click on the respective country that needs to be download (The country which are used in
this visualisation are India, Ireland, United States, Australia, China, Japan, UK, France,
Brazil and South Africa)
• The click on the download data in the page and select the download format of the file in
csv.
Step to download the population of all countries:
• Log in to the website http://data.worldbank.org/
3
• Click on the link ‘By Topic’ in the home page.
• Click on the respective topic (Total Population) that needs to be download (We will be
selecting the total population topic from the list of topics specified)
• The click on the download data in the page and select the download format of the file in
csv.
3.2 Processing
All the datasets which got downloaded from the world bank data center are in csv format. In the
data, we are having a lot of unwanted fields which will get filtered out.
In the visualisation we are using only the data from 2000 to 2015 but in the country wise csv file
there are data’s which are prior to that specified date. So these data need to be filtered out. And also there
are lot of topics in the country wise csv file other that ‘Mobile Cellular Subscriber’ and ‘Fixed Telephone
Subscriber’, which will also get filter out from the csv file. Similarly, the csv file for the population is also
filtered out and only the population on the specific county in use will be retained in the datasets.
We use Microsoft Excel to delete and filter out this dataset, because we are only deleting the
unwanted data from the dataset no additional complex cleaning process is need in this particular dataset.
3.3 Merging:
After filtering, the csv file will become much smaller in size and then the 11 datasets are merged
together. The column names will be in the order ‘Country Name’, ‘Country Code’, ‘Indicator’, and years
from 2000 to 2015.
Then the merged file will then get processed in Open Refine. Open refine is having a powerful
property called templating. This is used to convert the input file into a specific file structure the user needed.
Over here, the .csv file of different countries is pulled into the Open Refine and get template into a specific
format that we need. Then the file will get converted from .csv to json. So at the end of processing in Open
Refine, we will get a file which has the data of 10 counties arranged in the order we need in json format.
This json file will be the input for the data visualisation.
3.4 Initialising
In this visualisation we are calling the data from a webserver rather than placing it in a json file
locally. For that we will copy the code which we got as an output from open refine and place it in the
webserver http://myjson.com/2njqe [3]. Upon clicking the save button, the website will give you a link
which can be used as an input to the visualisation code which is written for creating the motion chart.
The tool which is used over here to create the visualisation is D3.js which is one of the most
powerful JavaScript library. The chart which is taken into consideration to create this beautiful visualisation
is the time series motion chart. The characteristic of the motion chart is that it will show a moving
visualization above a particular time period and in this case it will be from 2000 to 2015 which shows the
animation of Mobile cellular subscription vs Fixed telephonic subscription over the 15 years.

4. Result
Visualisation considered over here is a time series motion chart which is the best visualisation for
comparing two particular things happened over time. This chart will give a clear understanding of how
mobile subscription and telephone subscription evolved over the last 15 years.
In this chart we are taking 10 countries and comparing their Mobile cellular subscription and Fixed
telephone subscription. The x axis consists of the markings which represent the total number of Mobile
Cellular Subscription in that particular year. The y axis consists of the marking which represent the total
number of Telephonic Subscriptions. When loading the chart with the data its consist of 10 circles which
represent each country. As color scale is used in the code, each country will appear in different color in the
visualisation. The chart is laid out in such a way that if you mouse over the dots for the particular countries
the respective country name and population will get displayed. The size of the dots represents the population
of that particular country. The largest dot will represent the country with largest population and the smallest
one represent the smallest population. The dataset is hosted in a webserver, the d3.js will call the dataset
from the webserver, when the code gets loaded into the browser and display the respective values.
The code is designed in such a way that, when the html file is loaded for the first time, the data
transition happens from 2000 to 2015. There is a year label in the motion chart which describes the data
shown in the chart is of which year. The first load of the html page will trigger the automatic transition of
the year from 2000 to 2015. Only when the transition gets over we can mouse over the year label from left
to right for increment year transition and from right to left for decrement year transition. Interpolation is
used in this chart because the value of 2015 is not given in the dataset but the visualisation is from 2000 to
2015. This mouse over in year label is for analyzing the data in that particular year more deeply. Below
displayed is the screen shot of how the visualisation looks
Figure 1. Visualisation Screen Shot
The principle of data visualisation principle used over here are,
• Animation: It is applied over the time period when the html file is loaded, as the file will
automatically move from 2000 to 2015 in the first load of the page.
• Coloring: This principle used over here as each county has different color to represent themselves
form others. This principle is achieved by the use of color scale in the D3 code.
5
Some of the other principle [4] we applied over here are,
• Convey Meaning: Our visualisation have clearly conveyed a comparison between the subscription
of mobile and telephone over 15 years.
• Objectivity: The objectivity is clearly obtained over here as we create an efficient visualisation
over last 15 years on mobile and telephone subscription in a simple more understanding way.
• Encourage Interaction: In the visualization, mouse over function is used to enable interaction over
the year label and also there is a move over in each circles representing the country which displays
the country name and population.
When the html file is loaded we can clearly see that the mobile subscription and telephone subscription
in the year 2000 was below 1 billion for all the countries. But as the year progress we can see that there is
a tremendous growth in the mobile subscribers when compared to the telephonic subscribers. As we cross
the middle of the transition; the year 2010, we can see that subscription rate of mobile uses is almost all the
country except Ireland crossed the 10 million point. And also there is a slight growth in the telephonic
subscribers in all the countries. The year 2011 is the saturation point for the telephonic subscribers, after
2011, we can observe that there is a dip in the telephonic subscribers but the mobile subscriber’s growth is
still increasing but the growth has slowed down. From the year 2011 to 2015 people started disconnecting
the telephonic subscription because of that there is a slight decrease in the telephonic subscribers in the
chart. The other interesting fact is that Ireland is the only country which showed a slight decrease in the
mobile subscription from the year 2008 to 2010. When the chart reaches 2015 we can see that the India and
China has toped in its mobile subscribers list followed by US, Brazil, Japan etc. When it comes to telephonic
subscription we can see that US and China tops the subscription followed by other countries.
The size of the population also has a major role to play over here. Population of India and China is
much higher that other countries so in the chart we can see a visible growth over the mobile subscription.
Ireland also has a good growth in the mobile and telephonic subscription but as the population size is small
the growth is not that much visible in the motion chart.

