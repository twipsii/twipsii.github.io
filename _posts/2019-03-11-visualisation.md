---
layout: post
title: Visualisation with R
comments: true
---
<div style="font-weight:bold; margin-bottom:10px;">
{% if page.date %}<small>{{ page.date | date_to_string }}</small>{% endif %}
</div>
Today we looked at how to visualize data using `ggplot2`. It implements the layered grammar of graphics and is a core member of the tidyverse package. Visualization is a huge topic in data analysis and using it inappropriately can lead to false interpretations by the readers/viewers.

**R4DS Chapter 3: Data visualisation**

This chapter is about making different graphs with ggplot2. The following code template shows the general approach to making graphs:

```r
ggplot(data = <DATA>) + 
  <GEOM_FUNCTION>(mapping = aes(<MAPPINGS>))
```

\<DATA\> represents the dataset, \<GEOM_FUNCTION\> defines what type of graph we want to create and \<MAPPINGS\> define how the data is represented.

This template can be extended by adding layers on top of it, e.g. a facet grid or additional geom functions.

I added many example functions to my library on how to use ggplot with different geom functions.

**R4DS Chapter 28: Graphics for communication**

Here, the focus lies on how to finalize graphs for the export, e.g. labelling the axes or annotating some of the data points.

It is also possible to change the theme of a graph. There are several options to choose from, e.g.:

- `theme_bw()`: white background with grid lines
- `theme_minimal()`: minimal theme, no background
- `theme_dark()`: dark background for contrast

The cheat sheets mentioned in the next section cover most of this and I will add links of them to my library.

**Cheat sheets on the web**

There are great cheat sheets about data visualization with ggplot2 online which will definitely reserve a spot in my bookmarks. Why create new ones when there are already great examples available? Here are two of them:

- [Data Visualization with ggplot2](https://github.com/rstudio/cheatsheets/blob/master/data-visualization-2.1.pdf)
- [The Chartmaker Directory](http://chartmaker.visualisingdata.com/)