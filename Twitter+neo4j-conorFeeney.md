Analysing Twitter Data with Neo4j
======================================

 Neo4j is an open-source graph database implemented in Java and can be accessible from software written in other languages using the Cypher Query Language through a transactional HTTP endpoint. It is a ver popular graph database. It has been described as an ACID-compliant transactional database with native graph storage and processing. Neo4j was orgially released in February, 2010, and the company ia based in the San Francisco Bay Area, US and Malmö, Sweden.

There are many uses of Neo4j, and graph databases in general. I will now discuss several applications of using graph databases, specifically Neo4j, in order to analyse and store data and the benefits and cons of doing so.

####Master Data Management
 The world of master data is changing. Data architects and application developers are swapping their relational databases with graph databases to store their master data. This switch enables them to use a data store optimized to discover new insights in existing data, provide a 360-degree view of master data and answer questions about data relationships in real time. Business gain the benefit of real time insights into data, along with a place to store and model their data. Some challenges that can stem from this, however, are:
* **Complex and Hierarchical Datasets** are quite difficult to manage in this state. The code is difficult to build, slow to run and expensive and time-consuming to maintain.
* **Real-time Query Performance** Master data systems must integrate with and provide data to a host of applications within the business – often in real time. However, traversing a complex and highly interconnected data set to provide real-time information is a challenge, and often leads to slow responses if the data set is quite large.
* **Dynamic Structure** Master data is highly dynamic, with constant addition and re-organization of nodes, making it harder for developers to design systems that accommodate both current and future requirements. This is due to the changing nature of the nodes.

  Where Neo4j comes in, is here. The problem with relational database management systems is that they are no longer as efficient or useful for storing master data. Neo4j uses native graph storing, meaning,  it stores interconnected master data that is neither linear nor purely hierarchical. Due to this method of storing, indexing is not forced. In additions this makes accessing the data easier.



####Social Networks
 Whether you’re leveraging declared social connections or inferring relationships based on activity, graph databases such as Neo4j offer a world of fresh possibility when it comes to creating innovative social networks. Navigating a social graph and understanding both individuals and their relationships requires complex and deep queries. These particular queries bring most relational databases to their knees. Likewise, other types of NoSQL databases struggle to handle high degrees of relatedness. Graph databases are both easy and quick at traversing relationships, and they return instantaneous query results, making them an ideal choice for your social application.Social networks are already graphs, so there’s no point converting a graph into tables and then back again. Having a data model that directly matches your domain model helps you better understand your data, communicate more effectively and avoid needless work. Using Neo4j improves the quality and speed of development for your social network application.

<pre><code>
library(bitops)
library(RCurl)
library(RJSONIO)
library(twitteR)
library(ROAuth)
library(base64enc)

requestURL<-"https://api.twitter.com/oauth/request_token" 
accessURL<-"https://api.twitter.com/oauth/access_token" 
authURL<- "https://api.twitter.com/oauth/authorize"
consumerKey<-"V7OI2ptjiAj2tNXQCYMps03eV"
consumerSecret<-"EEnl077OCGo8s8XRlcQ4Q8kS62BZWIrnaonKQkZOJvp7oVK7sw"
accessToken<-"378108462-tGOwYC8IuL8XFILiUjwdcz1tigJB6oVDIIt1JyaS"
accessSecret<-"dXLtO3iwMbAeo0xAzDmJhjLD41be544wHiy2y84C7gAQS"
Cred <- OAuthFactory$new(consumerKey=consumerKey,
                         consumerSecret=consumerSecret,
                         requestURL=requestURL,
                         accessURL=accessURL,
                         authURL=authURL)
download.file(url="http://curl.haxx.se/ca/cacert.pem", destfile="cacert.pem")
Cred$handshake(cainfo = system.file("CurlSSL", "cacert.pem", package = "RCurl"))
setup_twitter_oauth(consumer_key=consumerKey, consumer_secret = consumerSecret, access_token = accessToken, access_secret = accessSecret)

</code></pre>

- item1 `functionname()`
- item2 `functionname2()`


####Getting Twitter Data
There are a number of ways to get Twitter data:
- ***Pay*** companies like Datasift, who have contracts, with Twitter to have access to the data. You pay per query, so the more queries you have, the more it will cost to download the data.
- ***Go direct*** to source, i.e contact Twitter
- ***R***, the open source statistical maths program, has the ability to create a *handshake* (put definition here) with Twitter. This enables you to download Twitter data at no charge. We will discuss the pro's and cons of this method now.

So this method involves a lot of patience. This is because there is a limit to how much data you can download at once, as opposed to other methods which let you download as much as you want at once provided you pay. This "handshake" requires a Twitter Application Interface, also known as an "API". From this, we get a Consumer Key, a Secret Consumer Key, an Access Token, and an Access Key.


####Analysing Twitter Data
  From here, we can load this data collected in R into Neo4j. As Twitter is a social network site, with nodes (users) having multiple in-degrees (followers) and out-degrees(following), Neo4j is a logical choice for grpahing this network. Graph databases are particularly well suited to capturing social data because they store data as nodes and edges. A study was carried out using Neo4j and Twitter. The data was stored on Neo4j as such: Twitter users, tweets, retweets and mentions. These ended up being the types of nodes.
As such, we look at some work done in this area. For our the coding rubric goes like this:

1. If a user tweets a new tweet, this is stored as a user node, a tweet node, and a ‘tweeting’ relationship between the nodes
2. If someone retweets the original tweet, the retweet and the person tweeting it are added as new nodes, and the retweeting user is connected via the tweet relationship to the retweet, and the retweet is connected via the retweet relationship to the original tweet
3. If a user mentions another user, the mention tweet is connected to both the user that tweets it and the user mentioned

This gives us a very powerful and economical way of harvesting the social graph. In the references below is a link to the graph of some of the following:
#### references:
http://www.sandtable.com/analysing-twitter-data-with-neo4j-2/
http://neo4j.com/use-cases/
