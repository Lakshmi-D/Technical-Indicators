# Moving Averages

>>> from pyspark import HiveContext
>>> hc=HiveContext(sc)
>>> from pyspark.sql.window import Window as win
>>> from pyspark.sql import functions as func
>>> df=hc.sql('select date,close from stocks')
>>> df=df.dropna('all')      #to drop the first row which has only NULL values
>>> winSpec=win.partitionBy().rowsBetween(0,9)
>>> ma=df.withColumn('movAvg',func.avg(df['close']).over(winSpec))

