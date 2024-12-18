---
layout: home
title: "The Case of America’s Beer Bias: A Sudsy Investigation"
subtitle: "Is Your State Swaying Your Sip?"
cover-img: "/assets/img/background.png"
---
# Introduction

Countries often claim that they have the “best” beer, in this article we are going to analyse the US and see if we can quantify a bias that people from different states have for each other's beers. Does the state you are from influence your beer preferences, especially towards beers coming from your own state? More generally, by examining the data from the Beer Advocate beer review website, we aim to uncover links between a user's geographical location, and how they rate beers. We were inspired by different regions of the world having similar food, so to try and find trends in beer data we’re going to start with a ‘regional’ analysis of states. Additionally, we will attempt to explain and find reasons for the bias in preference by looking at various factors, such comparing specifically neighbouring states, or analysing differences in beer style preferences.

# The data we used
We valued having large, high-quality datasets to uncover trends in beer preferences and biases. By looking at the distributions of beers and users by country/ state of origin in the Beer Advocate dataset, we were able to notice that most users came from the US. Not only this, but we can see that the more beers a certain country or state creates, the more reviews they have; for both local and non-local reviews. For this graph, we define local reviews as reviews where the user and beer of interest are from the same state/country. All other reviews are non-local reviews.
![Mon image descriptive](/assets/img/local_vs_non_local_reviews_by_country.png)
It’s interesting to note that there is a positive correlation between the number of beers that a state produces, the more local and non local reviews a state has. Indeed it seems that the bigger the state/country, the more beers it produces and also the more users on the website it has which further supports our need to select the US states as our geographical region of interest due to its abundance of data with regards to both users and beers. 
Moreover, after comparing the Beer Advocate and Rate Beer datasets, we observed that Beer Advocate was more focused on the US, aligning better with our goal of analyzing US-based geographical biases. 

# 1) Do regions like the same kind of beer?

# 2) Do we see significant differences between regions when comparing beer ratings?
After identifying trends within individual regions, we extended our analysis to compare beer ratings between regions. Our goal was to detect whether significant differences existed between how regions rated their own beers (in-region ratings) compared to beers from outside regions (out-region ratings). To quantify this, we used Cohen’s D, a statistical measure that assesses the standardized difference between two means. Cohen's D < 0.2 indicates a negligible difference. To explore regional biases in beer ratings, we conducted a two-part analysis:

## Neighboring bubbles analysis 

We first examined whether users in each neighboring  bubble showed preferences for beers in their bubble compared to outside. However, all Cohen’s D were below 0.2, meaning there was no statistically significant difference between the ratings.

## Custom region analysis
Next, we analyzed the regions we constructed earlier based on insights from the neighboring regions analysis of part 1 to see if we can see more trends. For these custom clusters, we compared in-region and out-region ratings using Cohen’s D. Again, all Cohen’s D values remained below 0.2, confirming that users did not rate beers from their own regions significantly higher.

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="/assets/img/question2/regional_on_question1.html" 
            width="1100" 
            height="1000" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>



