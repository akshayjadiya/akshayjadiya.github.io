---
layout: post
title: Customer Segmentation and Targeting
published: true
---

I have done a bunch of Segmentation & Targeting projects at my work and I aim to share my learnings through this blog post. 

This article will —
1.Cover the “What” , “Why” and “How” of the S&T process
2.Give you a walkthrough of a Segmentation project using a Kaggle dataset

So, let’s dive right in!
![_config.yml]({{ site.baseurl }}/images/config.png)

## What is Segmentation and Targeting?

I like to think of the Segmentation process as an **analytical way of classifying customers to optimize targeting efforts**. 
I have come across two types segmentation (although, there can be more) —

- **Behavioral Segmentation** — Done using ‘secondary’ data i.e. using historical data that captures the ‘behavior’ of a customer.
- **Attitudinal Segmentation** — Float a survey having questions directed towards assessing customer preferences.
The focus of this post will be on the Behavioral Segmentation.

**Targeting** is the process of using segment definitions and corresponding characteristics to **inform marketing decisions (frequency / channel / target value etc.)**. Targeting can be thought of **prioritizing segments in a way that aligns with the marketing strategy** and optimizes resources.


## Why Segmentation and Targeting is done?

There are three main reasons to leverage data and analytically derive segments —
1.It leads to **effective deployment of marketing tactics**
2.It **divides the customer universe into logical groups** that are easy-to-understand
3.It allows you to make **efficient use of the marketing budget** allocated to a specific channel

## The “How” of Segmentation

The best way to understand one of the ways to create segments is to show an example. You can find the code/dynamic excel file [here](https://github.com/akshayjadiya/HCPSegmentation) and get the data [here](https://www.kaggle.com/roamresearch/prescriptionbasedprediction)

> The data that I am using has the drug level prescriptions written by a doctor over a period of time. The dataset also captures some of the other physician characteristics such as specialty, years of experience etc. The goal is the divide the doctors into 4 different segments so that the sales representatives can visit them with varying frequencies — highest frequency to physicians in a group that is the most valuable and low/no visits to doctors in segments that are of low value.

If I have to summarize the overall process in 3 broad steps, they would be —
1. Identify customer characteristics that influence purchasing behavior
2. Rank customers on each of the identified dimensions
3. Define segments based on market understanding



The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.
