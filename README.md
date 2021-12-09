# NYC_Age_CrimeRate_difference_Heat_Map
data science project

# Project Data Science: NYC Age Crime Rate difference Heat Map: Project Overview

![title image](https://user-images.githubusercontent.com/56932664/145450968-e8cdd9ca-341a-4f6b-b92b-e7f7f81cfd9e.jpg)

# ABSTRACT
My focus for this project is to verify my preconceived notions about different age groups in NYC.\
My approach to solving this problem is by using data science to sort publicly avaiable crime data set. \
I used the age and plot them with the same threshold_scale using folium. Using the given borough names in the data set.

# OBJECTIVE
Use publicly avaibale police data that reports crimes in different areas around NYC. \
Then extract the data and make multiple choropleth maps using the same threshold_scale to see the difference \
of crime rate based on age in each NYC borough. 

# Hypothesis
My underlying hypothesis on this topic is people who just turn to adulthood commit more crimes. 

# Data Section
The data set I used is Public-Safety NYPD-Arrest-Data-Year-to-Date. 

Age group prrovided by the publicly avaiable data set is
<pre>
    AGE_GROUP
0     25-44 
1     18-24 
2     45-64 
3       <18 
4       65+ 
</pre>

The boroughs in the dataset includes
<pre>
          ARREST_BORO
0           Bronx
1            Kings county
2           Queens
3           Manhattan
4           Staten island
</pre>

Crime count of each borough based on age 

<pre>
            boro   <18  18-24  25-44  45-64  65+    
0          Bronx   931   5138  14496   4456  291 
1       Brooklyn  1070   6225  17635   5637  437 
2      Manhattan   681   4750  16448   6580  489 
3         Queens   586   4766  14156   4754  392 
4  Staten Island   140   1052   3111   1011   67 
</pre>

I also used a geojson file of the 5 boroughs in NYC called Borough Boundaries.
This geojson file has all the longitude and latitude of all 5 brorughs which allows use to create
a ChoroplethMap using folium.

# techniques section
I began by downloading the geojson file and the Public-Safety NYPD-Arrest-Data-Year-to-Date csv file. \
I downloaded/scraped the data using requests. I then read the files using pandas. \
After that I Change the name of the borough to its full name so I could plot them on the folium map. \
Then I filtered the data by using pandasql to create 5 different data frames based on certain age groups,inaddition \
to adding a count column displaying the total amount of crimes in each borough. \
Then I created a function called makeChoroplethMap using folium. Here I created 5 different ChoroplethMap shown below.

# Choropleth Maps
<18
![lessThan18](https://user-images.githubusercontent.com/56932664/145445364-f5dc5b9c-04db-4a14-a552-c2fd1eb35dd4.PNG)

18-24
![18-24](https://user-images.githubusercontent.com/56932664/145448326-c13250ef-1e4c-4989-9c6f-89a29469d1d8.PNG)

25-44
![25-44](https://user-images.githubusercontent.com/56932664/145448343-d7e1b965-8d4b-4c7c-974c-23091a0ace92.PNG)

45-64
![45-64](https://user-images.githubusercontent.com/56932664/145448371-6d86ad75-06ea-486c-a389-394b94772bb6.PNG)

65+
![65Plus](https://user-images.githubusercontent.com/56932664/145448391-219c5583-fc0b-4557-9904-ffbb4316c208.PNG)


# FINDINGS/RESULTS
With all the information I gatered by making choropleth map I found out that my hypothesis was wrong.
Instead ages 24-44 commit the most crime followed by 18-24 then 45-64 then <18 and lastly 65+ who commit the least amount of crimes. 

The list goes from highest to lowest based on each borough
<pre>
Bronx highest crime rate based on age 
1) 24-44 
2) 18-24 
3) 45-64 
4) <18 
5) 65+ 

Brooklyn highest crime rate based on age 
1) 24-44 
2) 18-24 
3) 45-64 
4) <18 
5) 65+ 

Manhattan highest crime rate based on age 
1) 24-44 
2) 45-64 
3) 18-24 
4) <18 
5) 65+ 

Queens highest crime rate based on age 
1) 24-44 
2) 18-24 
3) 45-64 
4) <18 
5) 65+ 

Staten Island highest crime rate based on age 
1) 24-44 
2) 18-24 
3) 45-64 
4) <18 
5) 65+ 
</pre>


# Citations Section
Python Code

Resources: geoJson file of NYC https://data.cityofnewyork.us/City-Government/Borough-Boundaries/tqmj-j8zm , 
Crime data set file https://data.cityofnewyork.us/Public-Safety/NYPD-Arrest-Data-Year-to-Date-/uip8-fykc ,
Background resources include the schoolChoropleth.py program you can find this in https://stjohn.github.io/teaching/data/fall21/work.html program 16
