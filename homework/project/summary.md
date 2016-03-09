##General Assembly Data Science 19 Final Project
###The Data
For my project, I wanted to use [Crunchbase data]( https://data.crunchbase.com/v3/page/accessing-the-dataset)  to attempt to build a model that would predict whether a company was public or private based on information such as funds raised, industry, number of employees, education background of founders, etc.  Crunchbase is a service that provides informations about funding and people in the startup ecosystem. In the past year, they launched a paid program for data access, so I was not able to use their API to use the data. Instead, I was able to gain access to historical data via the 2013 Snapshot, which provides data up through December 2013 in the form of multiple MySQL dump exports.
###Processing the data
In order to use the data, I wrote a Python script to convert the MySQL dump files into Pandas dataframes.
###Exploring the data
I learned that the data was very messy, there was a lot of missing data, and that there was a fundamental issue that I could not diagnose. When I joined tables by the primary key, there were very few matches, indicating that the data was likely not complete. Due to a lack of documentation available, I was not able to diagnose the problem further.
###Changing the Problem
I decided to just look at funding rounds, to see whether it is true that later funding rounds involve larger investments.
###Conclusion and Next Steps
There are many applications of predicting whether a company is public or private, especially if you add in the time component and predict when a company will go private. Unfortunately, this dataset was not sufficient to build a model to solve this. For someone who has access to the Crunchbase API, a next step would be to use the up to date data to build such a model. Alternatively, there may other data sources that could make this possible. 
While I knew that processing the data was often the bulk of the process, working on this project definitely drove the point home. After spending the time to obtain and proccess the data, it was dissapointing to find out that it was not sufficient to answer the original question.

