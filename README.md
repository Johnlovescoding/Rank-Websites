Simple Implementation of Ranking Webpages in Google Search Engine:
--------------

PageRank implementation with Java based in Hadoop ecosystem

Current model:
--------------
- PageRank algorithm

Reference:
----------
- "The Anatomy of a Large-Scale Hypertextual Web Search Engine", BSergey Brin and Lawrence Page, Computer Networks and ISDN Systems. 30: 107–117, 1998



Getting started:
----------------

First, start hadoop ecosystem.
Then run:

```Java
hdfs dfs -rm -r /transition 

hdfs dfs -mkdir /transition 

hdfs dfs -put transitionsmall.txt /transition 

hdfs dfs -rm -r /output* 

hdfs dfs -rm -r /pagerank* 

hdfs dfs -mkdir /pagerank0 

hdfs dfs -put pr.txt /pagerank0 

hadoop com.sun.tools.javac.Main *.java 

jar cf pr.jar *.class 

hadoop jar pr.jar Driver /transition /pagerank /output 30 

//args0: dir of transition.txt
//args1: dir of PageRank.txt
//args2: dir of unitMultiplication result
//args3: times of convergence
```

Notes:
------

