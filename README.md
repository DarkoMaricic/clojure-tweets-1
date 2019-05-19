# clojure-tweets

A Clojure Project designed to help in data science analysis of Tweets and Financial market indexes

## Usage

In order to use this application, you have to:
<ul>
1.Have Leiningen installed (for Windows users: http://leiningen-win-installer.djpowell.net/)
2.Have mongoDB installed https://www.mongodb.com/download-center/community
3.download the desired index/historical value datasheet from https://finance.yahoo.com as CSV. Edit the CSV file: date format needs to be in MM/dd/yyyy. Change all column names to be lowercase (date instead of Date, adjclose instead of Adjusted close etc.). Upload the CSV file to mongoDB and create data base SP (in the given example we evaluate Standard&Poor 500 index), and data collection Spider (S&P500 indexed ETFs nickname on WallStreet). In order to use other indexes, make sure you change the database and data collection name in .core namespace - getindex function.
</ul>

Start the application by navigating to the project folder in the console and type LEIN RUN [port number] (for example 7800).

You can now find the application on your browser by typing localhost:[port number].

The home page will look like this:
<img src="images/s1.PNG">

When you fill out the search form, press Submit.

You will get the tweets for the dates you entered, the tweet text and how the index (in this case S&P500) changed for that day.
<img src="images/s2.PNG">

The second tab will provide you with charts: Histogram, Line plot, and Scattered plot (made possible by Oz library).
<img src="images/s3.PNG">

Histogram and Colored Scatterplot are showing how many times did the index change up or down regarding the sentiment of the tweet.
The sentiment analysis in the application marks the tweet text as positive, neutral or negative (1, 2 o 3 respectively).
Finally, the line plot provides you with the index timeseries together with sentiment marks (1, 2 or 3) added on dates tweets were posted. Here you can track if the index changed and what was the tweet and its sentiment that day.

Next step of this application will be adding an option to generate the PDF report on the analysis that the user gets and to add multiple indexes for the analysis to be more precise (charts, tables and create report buttons). Stay tuned :)






## License

Copyright © 2019 

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
