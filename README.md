Saving huge amount of data on premises is too old and very dangerous. It is very expensive and time-consuming hardware. Querying the data can be very time consuming.

Google Cloud Platform introduces very fast and time efficient products. Google BigQuery is the enterprise data warehouse which is very fast as compared to on-premises machines. It gives the result in no-time.

The following lab is to explore BigQuery and get hands on experience.

**Explore Different data in BigQuery**

First log in to GCP platform, and from the navigation side menu, select BigQuery and pinned it too.


![Test Image 4]( https://github.com/acadali/Explore-a-BigQuery-Public-Dataset/blob/master/1.png)


After clicking BigQuery, click &quot;Add Data&quot; and explore public data.


![Test Image 4]( https://github.com/acadali/Explore-a-BigQuery-Public-Dataset/blob/master/2.png)


After selecting any public data, click &quot;View Dataset&quot;. In this case I have selected Austin Crime Data.


![Test Image 4]( https://github.com/acadali/Explore-a-BigQuery-Public-Dataset/blob/master/3.png)


In that dataset, there is another dataset of bikeshare in Austin. I used that dataset. Once the data is loaded, we can write the query in query section.

`1. select * from `bigquery-public-data.austin_bikeshare.bikeshare_trips`;`


![Test Image 4]( https://github.com/acadali/Explore-a-BigQuery-Public-Dataset/blob/master/4.png)


1. `select start_station_name, end_station_name,subscriber_type, sum(duration_minutes) as totaltime from ``bigquery-public-data.austin_bikeshare.bikeshare_trips``group by start_station_name, end_station_name,subscriber_type limit 10;`

![Test Image 4]( https://github.com/acadali/Explore-a-BigQuery-Public-Dataset/blob/master/5.png)

**Own Data**

First download the data from [http://www.ssa.gov/OACT/babynames/names.zip](http://www.ssa.gov/OACT/babynames/names.zip). Extract the file. Open the file and check the schema.

Now you will create a dataset on your own in BigQuery. In the resources tab, click on your project&#39;s name. Click on &quot;Create Dataset&quot;.

![Test Image 4]( https://github.com/acadali/Explore-a-BigQuery-Public-Dataset/blob/master/6.png)

Once we created a dataset, we have to create the table with the data.

![Test Image 4]( https://github.com/acadali/Explore-a-BigQuery-Public-Dataset/blob/master/7.png)

When click on create table, select the CSV file from your system which you have downloaded. And fill the other information like in the figure below. And click &quot;Create Table&quot;.

![Test Image 4](https://github.com/acadali/Explore-a-BigQuery-Public-Dataset/blob/master/9.png)

 `SELECT name, count FROM ``BabyNames.Names2018`` WHERE gender = &#39;F&#39; ORDER BY count DESC LIMIT 5`

![Test Image 4]( https://github.com/acadali/Explore-a-BigQuery-Public-Dataset/blob/master/9.png)
