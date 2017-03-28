---
layout: post
title:  "Boom Bust Index"
date:   2016-08-27
excerpt: "A data-driven look at Silicon Valley's housing prices."
image: images/Posts/BBI/boom-bust-index1.jpg
tag:
- data analytics
- web development
- real estate
---

<center><b>Boom Bust Index</b> is an unscientific visualization of Silicon Valley's housing prices and income values from 2010-2014.</center><br>

<iframe src="https://ghbtns.com/github-btn.html?user=gargium&repo=ATT-Big-Data-Challenge&type=star&count=true&size=large" frameborder="0" scrolling="0" width="160px" height="30px"></iframe>    

## Motivation
This summer, I was given the opportunity to participate in AT&T's Big Data Hackathon in San Francisco. The hackathon's aim is simple: utilize data in a way that could bring us one step closer to realizing the [#SmartCities Initiative](http://about.att.com/sites/internet-of-things/smart_cities). 

Smart Cities is a movement that seeks to make our cities more connected. Human beings generate [mind-boggling amounts of data](http://www.vcloudnews.com/every-day-big-data-statistics-2-5-quintillion-bytes-of-data-created-daily/), just by existing in today's world. We can leverage this data to create a framework that helps cities [become cleaner, safer, and more connected to their citizens.](http://about.att.com/sites/internet-of-things/smart_cities) The end result is a city that has the infrastructure and transparency to enrich the lives of everyone that lives and works there. 

Growing up in various parts of Silicon Valley, I've lived through moments of extraordinary change in the region's economic output and health. From the dot-com boom that brought my family here to the economic downturn that nearly halved the value of homes in the area, I've grown up steeped in a housing market that has been characterized by steep ups and downs. 

I thought it'd be cool to visualize these trends by pulling data from [DATA.GOV](https://www.data.gov), which has a treasure trove of information about various cities. It has census information, crime data, the amount of bicycle racks on every corner, and much  more. I used CitySDK, which can be found on DATA.GOV, and I highly recommend [checking it out](https://uscensusbureau.github.io/citysdk/) for your own projects! 

There are multiple factors that affect the valuation of a home, including local school APIs, crime rates, walkability scores, and proximity to industry. We can use census data to track home valuation growth and decline and gain insight into how well the supply of homes satisfies the demand from buyers. In the future, data like this could help urban planners figure out what neighborhoods to focus city resources on and better apportion public funds, thus increasing fiscal efficiency at the local municipality level. 

## Getting Up and Running
* Download the [Boom Bust Index on Github](https://github.com/gargium/ATT-Big-Data-Challenge)
* Fire up Terminal and navigate to `/static/Data/` within the repo.
* Run `./import.sh`
* Run `mongo`
* Navigate to the root directory in the repo and run `python app.py`
* Open your fav web browser and navigate to `localhost:5000`

## Features

#### Interactive Charts

<figure class="half">
    <a href="images/Posts/BBI/1.png"><img src="/images/Posts/BBI/1.png"></a>
    <a href="images/Posts/BBI/2.png"><img src="/images/Posts/BBI/2.png"></a>
    <figcaption>Charts displaying the income level and home values from 2010-2014 in Tract 500100 in Santa Clara County.</figcaption>
</figure>

#### Map Visualization
<figure>
    <a href="images/Posts/BBI/3.png"><img src="/images/Posts/BBI/3.png"></a>
    <figcaption>Google Maps with color-coded overlays to indicate the home value growth of every tract in Contra Costa, Santa Clara, and San Francisco counties.</figcaption>
</figure>

#### Index Calculation

BBI - Score
Generally speaking, a neighborhood that has everything going for it will have a score closer to 1, while a neighborhood with nothing going for it will have a score closer to -1. 

## Lessons Learned
Moving forward, I want to explore the reasons why families choose the homes they do, and how buying and selling real estate can become more streamlined and efficient. For starters, it seems rather obvious that a family would buy whatever real estate best fits their needs, but why must the home-buyer tolerate the formal process of finding an agent, viewing lots of homes, making lots of offers, and hoping that one goes through. This seems like an area ripe for disruption, especially if we could create tools that understand a buyer's life and can suggest homes that would fit the buyer's mold more accurately. 

Think about the way tird-party cookies work. I could look at a pair of sneakers on Amazon and then get bored and go to Facebook, and I'll still see ads for those sneakers in my Facebook sidebar! It doesn't matter what website I visit. Ad providers can track my information and suggest exactly what I want across multiple domains. 

If a model could understand a buyer's income, asset levels, occupation, and hobbies, it could suggest homes that are affordable and more likely to fit a buyer's needs instantly, solving the problem of finding homes to show a buyer in the first place. This information is not only a) volunteered by most users on a daily basis, but b) one could simply ask the buyer for it in exchange for a painless home-buying approach. 


(Update 12/2016: I'll be interning at [Redfin](https://www.redfin.com) during Summer 2017! I'll be shipping tools that help real estate agents and families buy and sell homes more easily.)

