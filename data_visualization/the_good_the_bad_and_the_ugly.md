the_good_the_bad_and_the_ugly
========================================================
author: Susann Bader    
date: 
autosize: true

Importance of data visualization
========================================================

- transformation of raw data tables into numeric illustrations
- reasoning about quantitative information

- communicate complex relationships
-  tendency to oversimplify --> limitation but also power



Anscombes Quartet
========================================================
- effectively makes the case that looking at summary statistics of data is 
insufficient to identify the relationship between variables.
- four different data sets (Anscombe’s quartet) which have nearly 
identical summary statistics. 
- All of them have identical descriptive statistics
- Never trust summary statistics alone; always visualize your data
-  data have the same mean and variance for x and y, 
same correlations between x and y, and 
same regression coefficients on the linear projection of x on y


```r
library(datasets)
datasets::anscombe
```

```
   x1 x2 x3 x4    y1   y2    y3    y4
1  10 10 10  8  8.04 9.14  7.46  6.58
2   8  8  8  8  6.95 8.14  6.77  5.76
3  13 13 13  8  7.58 8.74 12.74  7.71
4   9  9  9  8  8.81 8.77  7.11  8.84
5  11 11 11  8  8.33 9.26  7.81  8.47
6  14 14 14  8  9.96 8.10  8.84  7.04
7   6  6  6  8  7.24 6.13  6.08  5.25
8   4  4  4 19  4.26 3.10  5.39 12.50
9  12 12 12  8 10.84 9.13  8.15  5.56
10  7  7  7  8  4.82 7.26  6.42  7.91
11  5  5  5  8  5.68 4.74  5.73  6.89
```

```r
summary(datasets::anscombe)
```

```
       x1             x2             x3             x4           y1        
 Min.   : 4.0   Min.   : 4.0   Min.   : 4.0   Min.   : 8   Min.   : 4.260  
 1st Qu.: 6.5   1st Qu.: 6.5   1st Qu.: 6.5   1st Qu.: 8   1st Qu.: 6.315  
 Median : 9.0   Median : 9.0   Median : 9.0   Median : 8   Median : 7.580  
 Mean   : 9.0   Mean   : 9.0   Mean   : 9.0   Mean   : 9   Mean   : 7.501  
 3rd Qu.:11.5   3rd Qu.:11.5   3rd Qu.:11.5   3rd Qu.: 8   3rd Qu.: 8.570  
 Max.   :14.0   Max.   :14.0   Max.   :14.0   Max.   :19   Max.   :10.840  
       y2              y3              y4        
 Min.   :3.100   Min.   : 5.39   Min.   : 5.250  
 1st Qu.:6.695   1st Qu.: 6.25   1st Qu.: 6.170  
 Median :8.140   Median : 7.11   Median : 7.040  
 Mean   :7.501   Mean   : 7.50   Mean   : 7.501  
 3rd Qu.:8.950   3rd Qu.: 7.98   3rd Qu.: 8.190  
 Max.   :9.260   Max.   :12.74   Max.   :12.500  
```

Anscombes Quartet Nr 2
========================================================

![dinosaur_dozen](img/DinoSequentialSmaller.gif)


DataViz should tell a story
========================================================

- what is your incentive?
- story component is key






Graphical Integrity and Visual Perception
========================================================

- does the visual represent the underlying numbers?
- experiments on visual perception:

e.g. perceived area of a circle grows a bit more slowly than actual area:
perceived area = (actual area) ^ x x 0.8 =- 0.3

- perceptions differ
- perceptions change with experience
- perceptions are context-dependent



Lie Factor
========================================================

lie factor = size of effect shown in graphic / size of effect in data

example plot



Visual Area
========================================================

- do not use area for one-dimensional data
- elementary mistake of varying both dimensions in response to changes in one-dimensional data
- even worse when using three dimension to represent one-dimensional changes (volume of barrel)

example plot: shrinking doctor, corona stats munich

-> number of information-carrying variables depicted should not exceed the number
of dimensions in the data


Context Dependence
========================================================

- graphics must not quote data out of context

- show more data points to add context
- show comparible data



Inflation Adjustment
========================================================

- when plotting time series of money:
- value of money changes over time:
- make comparisons using inflation-adjusted units of money



Principles for Enhancing Graphical Integrity
========================================================

- physical measured surface of the representation of a number in a graphic 
(length of line) should be directly proportional to numerical quantity

- use clear, thorough labeling of the data on the graphic itself

- time-series of money should use deflated and standardized units

-  number of information-carrying variables depicted should not exceed the number
of dimensions in the data

- graphics must not quote data out of context



tables:
- actually show the numbers
- more efficient in communicating small dataset of less 20 numbers
- power of graphics comes with large datasets


The Good: Principles of Good Statistical graphics
========================================================

- data-ink ratio = 1.0 - proportion of graphic that can be erased without 
    loss of data-information
    
- data ink: not-erasable core of a graphic; 

- maximize the data-ink ratio
- erase non-data ink
- erase redundant data-ink 

example plot page 102


The Good: Chart Chunk
========================================================


The Bad: how to lie with charts
========================================================


- don't want to show you how to create deceiving figures
- but try to avoid common misleading interpretations
- inform your audience or dont show it at all


- Correlation is not causation
    - only posting falsely similar trends side-by-side when there is a reasonable explanation
- Similarities now don’t mean similarities forever (curves can bend, current date?)
- “Mean,” or average, is not the best go-to statistic
    - outliers can skew the data in one direction or the other
- the size of the axis, two axis plots with different scalings
- Abusing the Law of Large Numbers (LLN): 
    - show data points when there is little data
    - only large samples can provide trustworthy results
- 

Grammar of Graphics
========================================================

- take data values and convert them into visual elements
- map data values into quantifiable features (=aesthetics)
    - position
    - shape
    - size
    - color


References
========================================================
- https://clauswilke.com/dataviz/introduction.html
- https://www.autodesk.com/research/publications/same-stats-different-graphs
- https://damassets.autodesk.net/content/dam/autodesk/www/autodesk-reasearch/Publications/pdf/same-stats-different-graphs.pdf
