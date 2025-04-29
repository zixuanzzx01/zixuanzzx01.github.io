---
date: '2025-02-28'
draft: false
title: 'Detecting Neighborhood Migration Patterns in Chicago'
weight: 10
tags: ["Research"]
summary: "Chicago has always been a mosaic of shifting neighborhoods, but how they change — and why — is often hidden in thousands of rows of census data."

cover:
  image: "/images/test.jpeg" # Path to the image
  alt: "A descriptive caption for the image" # Alt text for accessibility and SEO
  caption: "Who moves where?" 
  relative: false # Set to true if the image path is relative to the page bundle
---

Chicago has always been a mosaic of shifting neighborhoods, but **how** they change — and **why** — is often hidden in thousands of rows of census data. In this project I set out to make those movements visible. Using recent American Community Survey (ACS) records and a dash of machine learning, I traced who is moving into each census tract, what makes those areas attractive, and how the picture has evolved between 2018 and 2023. Understanding these flows matters: migration reshapes the city’s economic life, housing market, and social fabric.

## From Raw Numbers to Migration “Fingerprints”

**Clustering the movers.**  I began with 36 variables that describe only one thing: *inflow* migration in 2018—how many people arrived, where they came from, and their income levels. Running K-means on a PCA-reduced version of that data uncovered five distinctive migration fingerprints without relying on any preset labels.

**Teaching the model to predict.**  Next, I asked whether everyday neighborhood features—median income, rent, rail access, education levels, and more—could *predict* those fingerprints. Machine Learning models, trained on 2018 data and tested on 2023, achieved moderate accuracy. The biggest signals?  
  * A high share of residents with a bachelor’s degree  
  * A large proportion of renter-occupied housing  

## What the Patterns Show

| Cluster label (brief) | Who’s moving in? | Typical origin | Income tilt |
|-----------------------|------------------|----------------|-------------|
| High-income magnet    | Professionals & managers | Within Cook County | Higher |
| External working-class hub | Service & trades workers | Out-of-state | Lower |
| Local working-class    | Similar income peers | Nearby tracts | Lower |
| Mixed inflow, extremes | Both very low & very high incomes | Mixed | Bimodal |
| Low inflow, stable     | Few newcomers | – | – |

*The labels are shorthand derived from centroid characteristics; see the full technical report for details.*  


## Chicago from 2018 to 2023: What Changed?

Between 2018 and 2023 many tracts **switched clusters**, underscoring how fluid neighborhood identities can be. Tracts that gained rapid rail access, for instance, often shifted toward high-income or mixed-income magnets. At the same time, some formerly popular areas cooled as median rents outpaced incomes.

<iframe src="/chicago_clusters_2018_interactive.html" class="embedded-content center" style="height: 700px; width: 100%;" ></iframe>

<iframe src="/chicago_clusters_2023_interactive.html" class="embedded-content center" style="height: 700px; width: 100%;" ></iframe>

## Want to Know More?

The full slide deck—including data sources, variable lists, and model diagnostics—is available **[here](https://github.com/zixuanzzx01/Detecting-Neighborhood-Migration-Pattern)**. I’m always happy to chat about the methods, limitations, or next steps.
