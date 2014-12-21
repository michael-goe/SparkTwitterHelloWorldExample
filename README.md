Spark Streaming with Twitter: A minimal example application
=============================

A minimal runnable Spark application using the Twitter Streaming API. Creates a Twitter input stream
and prints the first ten statuses of each one second interval (option one) or the first ten statuses
filtered by presence of their geolocation of each one second interval with their respective location
and status message (option two).

Please refer to the corresponding post on my blog for more information than the minimal instructions below: http://www.michael-goettsche.de/?p=19

### Setup
You will need to create an application at **https://apps.twitter.com/** (all you need is a normal Twitter account)
 to connect to Twitter and fill in the needed parameters from the **"Keys and Access Tokens"** page into *SparkTwitterHelloWorldExample.java*.

Also, you will need to have Spark installed.

### Build
Build with
> mvn compile assembly:single

### Run
Run with
> $SPARK_HOME/bin/spark-submit --class de.michaelgoettsche.SparkTwitterHelloWorldExample target/SparkTwitterHelloWorldExample-1.0-jar-with-dependencies.jar


Tested with: <br>
Spark 1.1.1 <br>
Java: 1.7 <br>
Maven: 3.2.3