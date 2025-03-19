
# Movie Data Analysis Dashboard





## Table of Content

 - [Project Overview](#project-overview)

 - [Data Sources](#data-sources)

 - [Findings](#results-and-findings)



### Project Overview

This project will analyze movies from 2012 to 2016 to find patterns, understand trends, and make recommendations based on the data.

### Data Sources

Movie Data: 

The main dataset for this analysis is the "Movie Data Homework.xmls" file, which includes detailed information about each movie's performance, actors, directors, and more.

[Download here](https://github.com/PolinaZhad/MovieData/blob/main/Homework10.xlsx)







### Tools



 - Power Query - Data Cleaning 

 - Excel, Pivot Tables - Data Analysis, Creating reports and visualizations



### Data Cleaning/Preparation



In the initial data preparation phase, we performed the following tasks:

1. Data loading and inspection.

2. Handling errors, missing values.

3. Data cleaning and formatting.



### Exploratory Data Analysis

1. Distribution of budget, revenue, and ratings to understand the range and identify outliers
2.  Most Profitable Genres
3.  Most Successful Actors

### Results and Findings

![Movies Data Dashboard](https://github.com/PolinaZhad/MovieData/blob/main/Screenshot%202024-07-29%20154140.png)



#### M Language 

One of interesting features I was working with was a specific code for Grouping in M language which enable me to Combine genres together for further analysis.

```

= Table.Group(#"Sorted Rows1", {"Movie Title"}, 

                                            {{"Combined Genre", each Text.Combine([Concat Genre], " / "), type text},

                                            {"AllData", each _, 

                                                        type table [Movie Title=nullable text, Release Date=nullable date, Wikipedia URL=nullable text, Concat Genre=nullable text, Director=nullable text, Actor First=nullable text, Actor Second=nullable text, Actor Third=nullable text, Actor Fourth=nullable text, Actor Fifth=nullable text, #"Budget ($)"=nullable number, #"Box Office Revenue ($)"=nullable number]}

                                            }

```


