---
layout: post
title: Data wrangling
comments: true
---
<div style="font-weight:bold; margin-bottom:10px;">
{% if page.date %}<small>{{ page.date | date_to_string }}</small>{% endif %}
</div>
This week marks the release of the long-awaited and infamous video about *Data wrangling*! It's a great summary of the chapters we read from the [R4DS](https://r4ds.had.co.nz/ "R for Data Science") book and shows explanatory examples on how to use the functions.

Tidying data is the basis of a good data analysis and will be a major part in our coding assignment. This is achieved by *wrangling* unstructured data. There are three simple rules which make a dataset tidy:

1. Each variable must have its own column.
2. Each observation must have its own row.
3. Each value must have its own cell.

The following image visualises these rules well:

![Tidy dataset](../../../data/images/tidy_dataset.png "Visualisation showing what makes a tidy dataset")

I already included most of the functions showed in the video in my library during the reading assignments. But now, that we have a video showing the usage of these functions, I added links to the functions in my Rmd files pointing to the corresponding timestamp in the video. I hope it doesn't get deleted!