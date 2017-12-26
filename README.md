# Technical-Indicators
Calculating moving averages

>>> from pyspark.sql import HiveContext
>>> hc = HiveContext(sc)
>>> df = hc.sql('select date,close from stocks')
