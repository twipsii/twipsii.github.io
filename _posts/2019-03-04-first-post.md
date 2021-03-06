---
layout: post
title: My first post, linear models and data structures
comments: true
---
<div style="font-weight:bold; margin-bottom:10px;">
{% if page.date %}<small>{{ page.date | date_to_string }}</small>{% endif %}
</div>
Dear reader, this is my first blog post describing the creation of my data analysis reference library in the course of the module **Quantitative Methods in Human-Computer Interaction** attended in the spring semester 2019. Future posts - which are hopefully created on a weekly basis - will cover additions to said library and describe how I was able to use its contents as a reference for my data analysis work.

**Creation and design**

For the format of my library, I decided to build up a collection of R Markdown files. I am planning to create one file for each major topic we deal with in the lecture. These files can be easily read in my preferred R tool: **RStudio**. The content and codes can be executed directly within RStudio. You can read more about the file format here: [R for Data Science - Chapter 27](https://r4ds.had.co.nz/r-markdown.html)

**Linear models**

Today we looked at how to formulate a linear model in R. Linear models are used to analyze the effect of categorical IVs to interval DVs. The general concept looks as follows:

Model function | Function in R
--- | ---
One IV | `lm(DV ~ IV, data = dataset)`
Two IVs | `lm(DV ~ IV1 + IV2, data = dataset)`
Two IVs with interaction | `lm(DV ~ IV1 * IV2, data = dataset)`
Two IVs, interaction, within-subjects design | `lmer(DV ~ (1|participant) + IV1 * IV , data = dataset)`

**R4DS Chapter 11: Data import**

R offers a handy package when it comes to importing, reading and writing data from/to files: `readr`. I added different ways to open different file formats to my library.

Regarding the values in the data file, it is important to parse the correct type of a value, e.g. string, integer, double or date.

Also, the encoding plays an important role when interpreting strings. The function `guess_encoding()` can guess the encoding of a string, which is pretty cool! When writing to files, we should always use UTF-8 encoding for strings, so the data is easily readable for others. There is a standardized format for date and date-times: ISO8601.

**R4DS Chapter 12: Tidy data**

There are three interrelated rules to create a tidy dataset, i.e. where the data belongs:

Type | Location
--- | ---
Variable | Column
Observation | Row
Value | Cell

`gather()` and `spread()` are two useful functions in the `tidyr` package to tidy data. `gather()` makes wide tables narrower and longer; `spread()` makes long tables shorter and wider.

`separate()` and `unite()` are also two complementary functions: `separate()` pulls apart one column into multiple columns, by splitting wherever a separator character appears, whereas `unite()` combines multiple columns into a single column.

I added examples and images of these to the library.

**R4DS Chapter 15: Factors**

When dealing with categorical values we can use factors. I added some examples using the *forcats* package to my library.

**R4DS Chapter 18: Pipes**

I've seen the pipe symbol `%>%` but I wasn't sure what it does. This chapter gives a good overview on how it works and what you can do with it. It makes a sequence of operations much easier to process (for the one who writes the code) and read.