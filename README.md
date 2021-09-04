# Covid-19 Analysis

### INTRODUCTION

Coronavirus disease 2019 (COVID-19) is a contagious disease caused by severe acute
respiratory syndrome coronavirus 2 (SARS-CoV-2). The pandemic has led to a dramatic loss of human life worldwide and presents an
unprecedented challenge to public health, food systems and the world economy.
The domain that we have chosen for our project is Data Analysis and under that our topic is
‘COVID-19 Data Analysis and Prediction’ as it is currently the most crucial and the most
relevant subject of discussion worldwide. The pandemic has been affecting all of our lives for
over a year now, but at the same time, it has given us, data enthusiasts, an opportunity to work
with a large amount of actual, real-time data, analyse it and draw some interesting
conclusions.

### OBJECTIVE
Our goal through this project is to use the data in a practical setting, perform some
manipulations on the data and gain insights from it. We have created interactive dashboards
tracking the number of cases, deaths, and recoveries – by country, based on the publicly
available COVID-19 dataset provided by Johns Hopkins University and another dashboard
tracking the cases in India, state-wise.

## Steps Followed
![Screenshot 2021-09-04 122010](https://user-images.githubusercontent.com/77155721/132085650-a7048462-82b3-4f86-bdc4-7e18d35b44c3.png)

### DATA COLLECTION
The data for our project has been collected from the GitHub data repository operated by the
Johns Hopkins University, Centre for Systems Science and Engineering (JHU CSSE).
We have taken three datasets which have a record of a cumulative number of ‘Confirmed
cases’, ‘Recovered cases’ and ‘Deaths’ on each date starting from 22nd January 2020 to up
until the day before, i.e., here, we are working on real time data. So, the data that we are
working on comes under the ‘Time Series’ data, i.e., collection of data at regular intervals in
terms of days, hours, months and so on.
Each dataset consists of columns, namely, Country, Province/State, Latitude, Longitude and
all the dates. In total, each of the three datasets have 350 columns (i.e., before transforming
the data).Each of the three datasets consists of approximately 250-300 row entries before data
cleaning and transformation.

![image](https://user-images.githubusercontent.com/77155721/132085701-49f3575a-ccfc-4db3-9061-c3049b25c9c2.png)

The other two datasets, i.e., the ‘Recovered cases’ dataset and “Deaths’ dataset have a similar
structure.

### Data Cleaning 
The process of removing or modifying data that is incorrect, incomplete,
unrelated, repeated or not formatted properly, in order to perform further analysis.
Firstly, we use the isnull() function to check for any null values in each of the datasets. This
will give us the total no. of null row entries in each column:


