---
layout: post
title:  "Why Does Climate Data Matter"
date: 2024-11-14
description: Data Science Blog post on finding the city with the warmest climate in the west 
image: "/assets/img/image5.jpg"
display_image: false  # change this to true to display the image below the banner 
---

## Introduction

Climate data matters significantly, as it affects our lives everyday. Weather can vary dramatically, especially on the West Coast. In my previous blog post I found the major city in the West with the warmest/most comfortable climate. In this blog we'll dive a little deeper into how I discovered this, and what that can mean.

## Key Insight 1: A Unique Climate

Through my previous data analysis we found that San Francisco had the warmest climate based on the composite score I came up with. This score used weighted factors of: temperature(50%), feels-like temperature(25%), and humidity(25%). Based on the high average temperature and feels-like temperature San Francisco was able to have the warmest climate even though it has a relatively low humidity. 

![Factor Comparison](/ds-blog/assets/img/insight1.png)

Based on the bar chart above we can see how San Francisco ranked compared to other West Coast cities

## Key Insight 2: Wind Speed and Cloud Coverage

Some of the other factors did have an effect on the climate even if they weren't included in the composite score. Wind speed and cloud coverage were two of the main factors. Cities like Boise, ID had a lower wind speed than other cities, which allows for a warmer climate compared to another city with a similar average temperature and higher wind speeds. Cloud coverage also makes a difference, as it leads to sunnier conditions and a warmer climate. Cities like Reno, NV have an advantage over other cities with similar average temps due to this factor. 

![Wind Speed](/ds-blog/assets/img/windy.png)

![Cloud Coverage](/ds-blog/assets/img/cloudy.png)

The graphs above show how the wind speed and cloud coverage of each city corresponds with the average temperatures.

## Streamlit App

To provide some additional insight into this dataset I've created a streamlit app. In this app you can explore the dataset I created in further depth. You can experiment with things like changing the weighting of the composite score, visualizing different factors, viewing the data for each city, or even adding in data for your own city. Feel free to check out the [streamlit app](https://willknisley-streamlit-lab-blog-post-l7qvmz.streamlit.app/). 

## Conclusion 

There are lots of insights to be pulled from this climate dataset, and it can be a great resource for someone looking to find their ideal city in the West. The streamlit app I've created will hopefully encourage others to experiment with this dataset. Those looking to explore this data with even more cities can through the app, and might be able to discover new and exciting insights. 

If you're interested in seeing the code I used to creating the visuals and the streamlit app check out [my github repository](https://github.com/willknisley/blog2/tree/main/post_3)