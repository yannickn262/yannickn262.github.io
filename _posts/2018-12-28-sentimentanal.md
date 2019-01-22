---
title: "Projects: Twitter Sentiment Analysis"
date: 2018-12-28
tags: [machine learning, data science, natural language processing]
header:
  image: "images/Sentiment/tsa.png"
body:
  image: "images/Sentiment/twcode.png"
excerpt: "Twitter Sentiment Analysis, Natural language processing"
---

Twitter Sentiment Analysis
### This project was first developed during the Summer'18. It was updated in the fall. The algorithm can calculate an accurate polarity score for up to a 1000 Tweets at a time. The score is from -1 which is the worst thing you can say about someone to 1 being the most positive thing. 

Sample Code:
```python
    while retry == True:
      keywordSearch = input("Enter a keyword/hashtag:  ")
      public_tweets = api.search(keywordSearch)
      noOfSearchTerms = int(input("Enter how many tweets to analyze: "))
      tweets = tweepy.Cursor(api.search, q = keywordSearch, lang = "English").items(noOfSearchTerms)
    #above line is responsible for creating filters as to how to narrow down search results
```
### Admittedly, I got this inspiration after watching a couple hours of  a random collection of  Youtube videos. I started by taking two portions of code from two separate videos. After the merging of both code bases and the inevitable build failure, I decided to start over and take certain aspects from each that I found most interesting. The authentication and enabling the Twitter API is a straightforward process that was identical in both. However, the development of the classifications of the polarity scores is what I modified the most. Moreover, I think the  pie chart through the Matplotlib library was the aspect that caused the most difficulty due to trouble relaying the data from the Twitter API into accurate color-coded proportions.
Python Sample Code:
```python
#this creates the pie chart
  labels = ['Positive ['+str(pos)+ '%]'], 'Neutral [' + str(neutral) + '%]', 'Negative [' + str(neg) +'%]'
  sizes = [pos, neutral, neg]
  colors = ['yellowgreen', 'gold', 'red']
  plt.pie(sizes, colors = colors, startangle = 90, autopct='%1.1f%%')
  plt.axis('equal')
```
