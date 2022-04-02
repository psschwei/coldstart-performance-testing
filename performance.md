# Test runs

## Using milliseconds

```
$ podspeed -prepull -pods 10 -template probe-milliseconds.yaml 
2022/04/01 20:08:12 Prepulling images to all nodes
2022/04/01 20:08:16 Prepulling done
Created 10 basic pods sequentially, results are in ms:

metric            |min  |max  |mean |median |p25  |p75  |p95  |p99
Time to scheduled |0    |13   |8    |8      |6    |10   |12   |12
Time to ip        |1977 |2071 |2011 |2001   |1988 |2028 |2050 |2050
Time to ready     |2975 |3058 |3010 |3008   |2984 |3024 |3046 |3046

```

## Not using milliseconds

```
$ podspeed -prepull -pods 10 -template probe-no-milliseconds.yaml 
2022/04/01 20:09:02 Prepulling images to all nodes
2022/04/01 20:09:06 Prepulling done
Created 10 basic pods sequentially, results are in ms:

metric            |min  |max  |mean |median |p25  |p75  |p95  |p99
Time to scheduled |0    |16   |8    |7      |4    |10   |15   |15
Time to ip        |1951 |2037 |2005 |1999   |1993 |2026 |2033 |2033
Time to ready     |3029 |4046 |3906 |3996   |3966 |4020 |4042 |4042

```
