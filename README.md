# NYC_Age_CrimeRate_difference_Heat_Map
data science project

# Project Data Science:ad NYC Age Crime Rate Heat Map: Project Overview

# ABSTRACT
My focus for this project is to verify my preconceived notions about different age groups in NYC.\
My approach to solving this problem is by using data science to sort publicly avaiable crime data set. \
I used the age and plot them with the same threshold_scale using folium. Using the given borough names in the data set. \

# OBJECTIVE
*Use publicly avaibale police data that reports crimes in different areas around NYC. \
*Then extract the data and make multiple choropleth maps using the same threshold_scale to see the difference \
of crime rate based on age in each NYC borough. \

# DATA GATHERED
Age group prrovided by the publicly avaiable data set \

    AGE_GROUP
0     25-44 \
1     18-24 \
2     45-64 \
3       <18 \
4       65+ 

Crime count of each borough based on age <br />
            boro   <18  18-24  25-44  45-64  65+
0          Bronx   931   5138  14496   4456  291
1       Brooklyn  1070   6225  17635   5637  437
2      Manhattan   681   4750  16448   6580  489
3         Queens   586   4766  14156   4754  392
4  Staten Island   140   1052   3111   1011   67


# Charts
![lessThan18](https://user-images.githubusercontent.com/56932664/145445364-f5dc5b9c-04db-4a14-a552-c2fd1eb35dd4.PNG)

# FINDINGS/RESULTS

With all the information I gatered by making choropleth map I found out that

The list goes from highest to lowest

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


# RESOURCES
Resources: geoJson file of NYC https://data.cityofnewyork.us/City-Government/Borough-Boundaries/tqmj-j8zm , 
Crime data set file https://data.cityofnewyork.us/Public-Safety/NYPD-Arrest-Data-Year-to-Date-/uip8-fykc ,
Background resources include the schoolChoropleth.py program you can find this in https://stjohn.github.io/teaching/data/fall21/work.html program 16
