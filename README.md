# Covid-19 Analysis

![e446a8e6-ce5c-49e8-a4a8-fc53eee02a0d_1920x1080](https://user-images.githubusercontent.com/77155721/132086452-870626e7-4bf8-466d-843f-a67e5eec6b50.jpg)


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

![Screenshot 2021-09-04 122455](https://user-images.githubusercontent.com/77155721/132085760-65d12114-0f8a-43f4-8217-b4cff458c38f.png)

We see that there are 65,394 null values present in the Province/State column. In order to treat
these null values, we fill it in with the values present in the corresponding Country/Region
column

### DATA TRANSFORMATION
After cleaning the data, the next step is transforming our data into a desired format. By
definition, data transformation is the process of converting data from one format or structure
into another format or structure.
In our datasets, the dates are in the form of columns. For the purpose of calculating the
confirmed cases, recovered cases and deaths on a daily basis, we need to transform the date
columns into row entries, or so to say, unpivot the date columns. For that, we use the melt()
function in pandas.
In the code given below, we write the names of the columns that we want to fix in ‘id_vars’
and rest of the columns then get unpivoted. In this case, all the date column headers get
converted into row entries under the column that we have named using ‘var_name’ as ‘Date’.
![Screenshot 2021-09-04 122653](https://user-images.githubusercontent.com/77155721/132085802-84537463-0ff5-4d13-8417-9f44710407dd.png)


###  DATA MERGING
Further, we join the three datasets into a single dataset so that it’s easier to work with. We use
the merge() function on the ‘Confirmed cases’ dataset and the ‘Deaths’ dataset and merge
them together into a single dataset. Next, we merge that dataset with the ‘Recovered cases’
dataset. Finally, we have all the three datasets merged into a single dataset.
![Screenshot 2021-09-04 122846](https://user-images.githubusercontent.com/77155721/132085841-a6b99faa-01fc-4814-aad5-9899508276f1.png)

Next, we perform some calculations on our data to derive the daily numbers from the
cumulative numbers. Fundamentally, we subtract the total no. of cases on a particular day
from the total no. of cases recorded on the next consecutive day, which gives us the daily
records that we would want.

![image](https://user-images.githubusercontent.com/77155721/132085859-f199ca08-5c13-4d1d-90dc-e2709310bde1.png)

Now that our dataset is in perfect condition for further analysis after we have cleaned and
transformed it, we export the transformed data to an Excel file and import it into Power BI for
data visualization.

### For Data Analysis and visualization I uesd Microsoft PowerBI and the link for the two dashboards is provided below:


https://drive.google.com/file/d/1pJCX5SxIJHMsjKFPRkBJhxa2sJpujOfN/view?usp=sharing



