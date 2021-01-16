# How to monitor smart devices at your home 

## Introduction 

In August 2020 I participated in a class in the Master's program in Computer Engineering at COPPE, this was during my senior year as a graduation student in Computer and Electronics
Engineering. This class was focused in Big Data, teaching us about Hadoop and more deeply about Apache Spark. The final avaliation was to develop a system using graphic interface(or
not), but using Spark as an ETL tool.

Also since it was a Big Data class we had to choose a project that attended two of the 5 V's of Big Data: Volume, Velocity, Variety, Veracity and Value. In a nutshell, these are the five 
keys to make big data an A-thing at your company. The 5V's are resumed below:

  * Volume: Your project must have a huge volume of data. We're not talking about Gigabytes, instead something like Terabytes(1000x Gigabytes) or Petabytes(1000000x Gigabytes) of data; 
  * Velocity: Since we have a lot of data, we must process these in a high velocity to make it able to be used;
  * Variety: The data must come from a different data sources;
  * Veracity: The data must be authentical, which means they must be true;
  * Value: The data that you're trying to use must have some use, otherwise you're pulling data from a source for no reason.
  
 Nowadays, it has been talked in [7V's](https://impact.com/marketing-intelligence/7-vs-big-data/) or even [10 V's](https://tdwi.org/articles/2017/02/08/10-vs-of-big-data.aspx). But
 in order to make it simple, we'll stay on the 5V's.

## Technologies 

Since we have to create an ETL tool and was suggested to create a graphic interface, I choose to clean the data and show it on [Power BI](https://powerbi.microsoft.com/en-us/desktop/) (you might have guest this due the title and the word "monitor").
Also, I had to clean the data before transmiting it to the Microsoft Tool, to do that I used [databricks](https://databricks.com/) which is a [Jupyter Notebook](https://jupyter.org/) that works on the cloud, this fact helps you if you're working with a teammate. Moreover, PowerBI has an API which will help connect the cleaned data and show it as a report. To clean the data I use [Pyspark](https://spark.apache.org/docs/latest/api/python/index.html), focused on the SparkSQL which helped me clean the data as if it was a SQL querie 

## The project

As I said in the beginning of the text, this project was made as an assignment to a class that I attended. So, the point here was to create an ETL project and show it as a web interface. I choose to work with IoT data, since it's a great source for huge amount of data and it needs to be consumed fast(therefore fulfilling 2 of the 5V's of Big Data: volume and velocity). Unfortunately I did not have IoT sensors at my house, so I search for datasets on [Kaggle](https://www.kaggle.com/) and found one with data enough to be used on this project. 

One challenge here was to connect Power BI with my databricks code, and to do that I used Power BI API. I had to generate a URL that connect to the dashboard, and passed each data as a json(since this the format accepted by the program), to simulate the streaming happening I sent one row at a time.  


## Results

The final result was a dashboard that looked like this

![image](/images/dashboard.PNG)
