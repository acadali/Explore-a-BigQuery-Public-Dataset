Saving huge amount of data on premises is too old and very dangerous. It is very expensive and time-consuming hardware. Querying the data can be very time consuming.

Google Cloud Platform introduces very fast and time efficient products. Google BigQuery is the enterprise data warehouse which is very fast as compared to on-premises machines. It gives the result in no-time.

The following lab is to explore BigQuery and get hands on experience.

**Explore Different data in BigQuery**

![image info](./Desktop/1.png)

First log in to GCP platform, and from the navigation side menu, select BigQuery and pinned it too.

![](RackMultipart20201001-4-1p3iabj_html_185694821e3a9f28.png)

After clicking BigQuery, click &quot;Add Data&quot; and explore public data.

![](RackMultipart20201001-4-1p3iabj_html_496b95cf7cfcc5ad.png)

After selecting any public data, click &quot;View Dataset&quot;. In this case I have selected Austin Crime Data.

![](RackMultipart20201001-4-1p3iabj_html_83f31abda8e32fc8.png)

In that dataset, there is another dataset of bikeshare in Austin. I used that dataset. Once the data is loaded, we can write the query in query section.

1. select \* from `bigquery-public-data.austin_bikeshare.bikeshare_trips`;

![](RackMultipart20201001-4-1p3iabj_html_ce3790f96b560dda.png)

1. select start\_station\_name, end\_station\_name,subscriber\_type, sum(duration\_minutes) as totaltime

from `bigquery-public-data.austin_bikeshare.bikeshare_trips`

group by start\_station\_name, end\_station\_name,subscriber\_type

limit 10;

![](RackMultipart20201001-4-1p3iabj_html_907a668ad0a68004.png)

**Own Data**

First download the data from [http://www.ssa.gov/OACT/babynames/names.zip](http://www.ssa.gov/OACT/babynames/names.zip). Extract the file. Open the file and check the schema.

Now you will create a dataset on your own in BigQuery. In the resources tab, click on your project&#39;s name. Click on &quot;Create Dataset&quot;.

![](RackMultipart20201001-4-1p3iabj_html_dfcca58341f2d8a0.png)

Once we created a dataset, we have to create the table with the data.

![](RackMultipart20201001-4-1p3iabj_html_d2bf831714e32811.png)

When click on create table, select the CSV file from your system which you have downloaded. And fill the other information like in the figure below. And click &quot;Create Table&quot;.

![](RackMultipart20201001-4-1p3iabj_html_84094d869eb6744.png)

1. SELECT name, count FROM `BabyNames.Names2018` WHERE gender = &#39;F&#39; ORDER BY count DESC LIMIT 5

![](RackMultipart20201001-4-1p3iabj_html_4980688b8ef6a9fe.png)
