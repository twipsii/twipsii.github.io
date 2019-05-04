---
layout: post
title: Sechseläuten and data transformation
comments: true
---
<div style="font-weight:bold; margin-bottom:10px;">
{% if page.date %}<small>{{ page.date | date_to_string }}</small>{% endif %}
</div>
No lecture this week due to Sechseläuten bank holiday in Zurich. Thankfully, we still got a reading assignment to do so that we don't get bored during the week without QuantHCI class... 🙄

**R4DS Chapter 5: Data transformation**

This chapter presents five key functions of the *dplyr* package that help in manipulating data frames:

- `filter()`: filters data basd on their values
- `arrange()`: reorders the rows
- `select()`: selects variables by their names
- `mutate()`: creates new columns based on existing values
- `summarise()`: collapses multiple values to a single summary

All these functions work similarly:

`function(data, what_to_do_with_data)`

There are good examples of these functions in this chapter using the *nycflights13* data set. I added some of them to the library, where I think they could be helpful in future data transformation tasks.