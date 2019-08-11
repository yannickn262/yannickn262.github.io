---
title: "Projects: Webscraping Real Estate Data"
date: 2018-12-28
tags: [Pandas, Data Science, Webscraping]
header:
  image: "images/jax.png"
body:
  
excerpt: "Webscraping Real Estate Data, using Realtor.com on Jacksonville Area"
---

Webscraping Real Estate Data

<img src = "assets/images/realestate.png" class = "inline" alt = "real estate output picture" style = "width:600px; height:500px;" />
### This project was created under the direction of Arduit Slice's Udemy Course. Initially, I was using Zillow as the primary source of data. Despite the numerous attempts to trick them into thinking that my program was a web browser I had no luck. After I changed my data source to realtor.com, things progressed more smoothly. Figuring out the exact unordered list item to scrape was a bit arduous, however it ultimately got the results I wanted.

Example:
```python
      try:
      #get number of bathrooms
        hash["Baths"] = item.find("ul", {"class": "prop-meta ellipsis"}).find_all("li")[1].find("span",{"class":"data-value"}).text.replace(" ", "")

      except:
        hash["Baths"] = "None"
        pass
```

### The project scrapes data from Realtor.com and outputs the data into a CSV file. This project could be developed further if it had a simple interactive UI that allowed users to enter the location instead of it being set automatically to Jacksonville.
