# Recommender-System
### Get into Hadoop

`cd src` 

### Get into Project

`cd RecommenderSystem`

`hdfs dfs -mkdir /input`

`hdfs dfs -put input/* /input` 

`hdfs dfs -rm -r /dataDividedByUser`

`hdfs dfs -rm -r /coOccurrenceMatrix`

`hdfs dfs -rm -r /Normalize`

`hdfs dfs -rm -r /Multiplication`

`hdfs dfs -rm -r /Sum`

`cd src/main/java/`

`hadoop com.sun.tools.javac.Main *.java`

`jar cf recommender.jar *.class`

`hadoop jar recommender.jar Driver /input /dataDividedByUser /coOccurrenceMatrix /Normalize /Multiplication /Sum`

`hdfs dfs -cat /Sum/*`

#args0: original dataset

#args1: output directory for DividerByUser job

#args2: output directory for coOccurrenceMatrixBuilder job

#args3: output directory for Normalize job

#args4: output directory for Multiplication job

#args5: output directory for Sum job
