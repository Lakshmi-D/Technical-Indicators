Cloudera version 2.6.0-cdh5.12.0
Spark version 1.6.0
Source file (EOD-JPM.csv) is the historical stock data of JP Morgan which contains stock data from 12/30/1983 to 10/6/2017. There are 8516 records and row names are as follows Date,Open,High,Low,Close,Volume,Dividend,Split,Adj_Open,Adj_High,Adj_Low,Adj_close,Adj_Volume
EOD-JPM.csv is shared from local to Cloudera VE (path = /media/sf_project/EOD-JPM.csv )
Source file is moved from Cloudera to HDFS using cmd: hdfs dfs -put /media/sf_project/EOD-JPM.csv
Created external table named Stocks in Hive with same column names as in source file.
Loaded data from source file located in hdfs into newly created table stocks. 


