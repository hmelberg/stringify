# Stringify
Analyse and visualize patterns of events

Transforms information from a database of prescriptions and other health events for each person to a string and adds tools to analyse these strings. The tools can answer questions like:
* How many persons receive pharma X before pharma Y?
* How many times is there an overlap between the use of pharma X and pharma Y?
* How many have a hospital event, for instance an ER event with stroke, within 100 days after ending their treatment of pharma X?
* How many people have pauses longer than 3 months in their use of pharmaceutical X?
* How many stop using pharma X after one prescription?


# Examples

 ```stringify(prescription_data, pharma_code_x)```


id |  pattern
---|---------
1 | xxx  xxx xx  x
2 |      xx     x
3 |   x     x     x

 ```pattern.count_events('xx')```
  
  id |  #pattern
---|---------
1 | 3
2 | 1
3 | 0

 ```stringify(pharma_code_y)```


id |  pattern
---|---------
1 | yyyyyyyyy
2 |     yyyyy
3 |     y   

 ```count.overlap(pattern_x, pattern_y)```
id |  #overlap
---|---------
1 | 9
2 | 5
3 | 0   

  
  
