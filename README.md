# Hadoop-MapReduce
MapReduce is the processing layer of Hadoop. MapReduce programming model is designed for processing large volumes of data in parallel by dividing the work into a set of independent tasks. You need to put business logic in the way MapReduce works and rest things will be taken care by the framework. Work (complete job) which is submitted by the user to master is divided into small works (tasks) and assigned to slaves.

![map reduce](https://www.tutorialspoint.com/hadoop/images/mapreduce_algorithm.jpg)

MapReduce program executes in three stages, namely map stage, shuffle stage, and reduce stage.

## Map stage −
The map or mapper’s job is to process the input data. Generally the input data is in the form of file or directory and is stored in the Hadoop file system (HDFS). The input file is passed to the mapper function line by line. The mapper processes the data and creates several small chunks of data.

## Reduce stage −
This stage is the combination of the Shuffle stage and the Reduce stage. The Reducer’s job is to process the data that comes from the mapper. After processing, it produces a new set of output, which will be stored in the HDFS.

## Basic implementations of MapReduce programs
# 1. Word Count Program :
We will count the no. of words in a file(in HDFS) and no of occurences we get will be stored in a seperate file in HDFS < [name of Output dir mentioned in command]/part* >

# 2. Word Count Program Using Tool Runner :
We will count the no. of words/occuraces of word in a file using a special function ToolRunner(in HDFS)and the file we getas output will be stored in HDFS < [name of Output dir mentioned in command]/part* >

# 3. Char_Count :
No. of occurances per charachter including all speccial charachters will be counted and stored in a file < [name of Output dir mentioned in command]/part* >

# 4. Word_Length :
Length of each unique word will be counted and stored in output file in HDFS < [name of Output dir mentioned in command]/part* >

# 5. Avg_Word_Length :
Average Length of each unique word on the basis of thier first letter will be counted and stored in output file in HDFS < [name of Output dir mentioned in command]/part* >

For example- if we have two word in a file named Hadoop and Hive then the output will be

    hadoop - 6 and hive - 4 => 6+4 => 10/no.of words
    output =>  h    5 

# 6. No. of Hits per IP Address :
Number of Hits on each unique IP Address on the basis of weblogs will be counted and stored in output file in HDFS < [name of Output dir mentioned in command]/part* >

# 7. WordCount Using Combiner Class :
A new Class is added in Driver code of the program making execution fast.Combiner class gets executed just after mapping phase and aggregates the data to help reducer in faster execution.

# 8. MRUnit Testing the MapReduce Code :
Just like there is a testing tool in java "JUNIT" there is "MRUnit" in MapReduce to test whether the code is running properly or not. We can test code by passing sample inputs and check the outputs.

# 9. Hadoop Streaming :
Hadoop Mapreduce is not limited to java it also supports various programming language like python perl and many other languages with the help of hadoop streaming libraries.

# 10. Hadoop Log Processing :
Since it is a Map only task it includes only mapper and a driver to process access logs. It finds the n.o of Hits per Image format on a particular site.

# 11. Hadoop Custom Partitioner :
Implementing a custom partitioner helps us customising partitioners according to the requirement of the user and storing customised data in different Reducers.
