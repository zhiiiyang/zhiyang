---
authors:
- admin
date: "2019-04-04"
draft: true
gallery_item:
image:
  caption: 'Photo by Charles 🇵🇭 on Unsplash'
  focal_point: ""
  preview_only: false
title: 'How to prepare for data scientist interviews with an eCommerce company'
subtitle: 'by reading helpful articles online'
summary: A short summary of what I've learned from preparing an interview with an eCommerce company
tags:
- R
- Data science
---

## Background

I didn't come up with any of those original contents. Here is just a summary of what I've summarized by learning from reading others' insights in how data science contribute to the growth of eCommerce companies and what challenges we are faced with while working as a data scientist at the company. 

## [5 Data Science Projects Every E-commerce Company Should Do](https://towardsdatascience.com/5-data-science-project-every-e-commerce-company-should-do-8746c5ab4604)

In this article, the author talked about five important DS projects that should be undergoing at every eCommerce company. I happened to know some of them but didn't realize about the full scope of it. I'll try to elaborate more details about how I've viewed each topic based on the interview techniques suggested by the Pramp.com ([see my previous article](https://zhiyang.netlify.com/post/pramp2/)). I will start with **identifying the goal** of the company, i.e., the rate of successful booking, followed by **specifying the most informative variables** to boost that metric, i.e., information from the client and browsing habits, and browsing history. And I proceed with **selecting several models** to achieve better prediction of the metric. 

- *Recommendation systems*
    Companies care very much about the success rates of customers clicking links, adding products into carts and complete purchases. Those can be reflected by the rating or the preference from a user. We can look up information from past searches, previous purchases and information of customers (i.e., location, education level, gender, and etc.). It comes much easier to pick the models for this scenario: collaborative filtering, content based filtering, and hybrid filtering. 
    
- *Customer lifetime value modeling*
    To be honest, I can conceptually understand its important but fail to concretize this idea or even give a mathematical definition of it. 

- *Fraud detection*
    This is probably the most familiar topic to me because I had some exposure from the machine learning class that I took at USC. It is of course very important and will directly have severe impact the efficiency. Of course, the outcome, that we care the most, is whether the purchase made this time is fraud or not. Essentially, there are lots of variables available for us to detect this abnormality, i.e., different locations detected while login-in, unusual purchase category, different shipping/billing addresses, unusual large orders of the same item, international orders and etc. The models, that could potentially useful to be adopted, include simple logistic regression, time series analysis, clustering and classification (logistic regression), matching algorithms. In this case, we can provide a safer environment for customers to increase their retention and increase company revenue. 
    
- *Important reviews*
    This topic comes into two perspectives: 1) we've already have established system to measure the scale of customers' satisfaction. 2) we need to use natural language processing skills to extract those information and quantify them. Then, visualization tools like WordClouds could be potentially helfpul and further be used for sentiment analysis. In a long run, we can maximize usrs' satisfaction and increase the retention rate, leading to maximizing the revenue and potential social impact. 
    

