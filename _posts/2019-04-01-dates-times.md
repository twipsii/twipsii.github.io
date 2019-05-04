---
layout: post
title: Dates and times
comments: true
---
<div style="font-weight:bold; margin-bottom:10px;">
{% if page.date %}<small>{{ page.date | date_to_string }}</small>{% endif %}
</div>
During this week's lecture I was able to use my library to analyse the data from Fitt's law study. The first part of the code was given and we had to extend it for an additional analysis. For this, we used parts from linear models and ggplot2.

**R4DS Chapter 16: Dates and times**

Working with dates and times is always overly complicated because of many factors:

- there are different time zones (and not all are full hour offsets)
- not every year has the same amount of days (365 vs. 366)
- daylight savings time two times a year in some parts of the world
- no decimal system: 60 seconds make a minute, 60 minutes make an hour, 24 hours make a day, and so on
- to be continued ...

This chapter presented some ways how to tackle these problems in R. But somehow, it gets even more confusing... There are data structures for time spans, this includes durations, periods and intervals.

In a nutshell, you have to be very cautious when working with dates and times. Normalise them to a format that works well for your problem.

I added some examples from the book to my library that I think could be helpful for future work with dates and times.