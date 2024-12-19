---
layout: home
title: "The Case of America’s Beer Bias: A Sudsy Investigation"
subtitle: "Is Your State Swaying Your Sip?"
cover-img: "/assets/img/background.png"
---
# Introduction

Countries often claim that they have the “best” beer, in this article we are going to analyse the US and see if we can quantify a bias that people from different states have for each other's beers. Does the state you are from influence your beer preferences, especially towards beers coming from your own state? More generally, by examining the data from the Beer Advocate beer review website, we aim to uncover links between a user's geographical location, and how they rate beers. We were inspired by different regions of the world having similar food, so to try and find trends in beer data we’re going to start with a ‘regional’ analysis of states. Additionally, we will attempt to explain and find reasons for the bias in preference by looking at various factors, such comparing specifically neighbouring states, or analysing differences in beer style preferences.

<div style="display: flex; justify-content: center; gap: 10px;">

  <!-- Première image -->
  <div>
    <img src="assets/img/image_budweiser.jpg" alt="Image 1" style="width: 300px; height: auto;">
    <p style="text-align: center;">Légende pour Image 1</p>
  </div>

  <!-- Deuxième image -->
  <div>
    <img src="assets/img/we_want_beer.jpg" alt="Image 2" style="width: 300px; height: auto;">
    <p style="text-align: center;">Légende pour Image 2</p>
  </div>

  <!-- Troisième image -->
  <div>
    <img src="assets/img/taste_the_high_country.jpg" alt="Image 3" style="width: 300px; height: auto;">
    <p style="text-align: center;">Légende pour Image 3</p>
  </div>

</div>

# The data used
We valued having large, high-quality datasets to uncover trends in beer preferences and biases. By looking at the distributions of beers and users by country/ state of origin in the Beer Advocate dataset, we were able to notice that most users came from the US. Not only this, but we can see that the more beers a certain country or state creates, the more reviews they have; for both local and non-local reviews. For this graph, we define local reviews as reviews where the user and beer of interest are from the same state/country. All other reviews are non-local reviews.
![Mon image descriptive](/assets/img/local_vs_non_local_reviews_by_country.png)
It’s interesting to note that there is a positive correlation between the number of beers that a state produces, the more local and non local reviews a state has. Indeed it seems that the bigger the state/country, the more beers it produces and also the more users on the website it has which further supports our need to select the US states as our geographical region of interest due to its abundance of data with regards to both users and beers. 
Moreover, after comparing the Beer Advocate and Rate Beer datasets, we observed that Beer Advocate was more focused on the US, aligning better with our goal of analyzing US-based geographical biases. 

# 1) Do regions like the same kind of beer?

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="/assets/img/question1/custom_region.html" 
            width="2000" 
            height="700" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

# 2) Do we see significant differences between regions when comparing beer ratings?
After identifying trends within individual regions, we extended our analysis to compare beer ratings between regions. Our goal was to detect whether significant differences existed between how regions rated their own beers (in-region ratings) compared to beers from outside regions (out-region ratings). To quantify this, we used Cohen’s D, a statistical measure that assesses the standardized difference between two means. Cohen's D < 0.2 indicates a negligible difference. To explore regional biases in beer ratings, we conducted a two-part analysis:

## Neighboring bubbles analysis 

We first examined whether users in each neighboring  bubble showed preferences for beers in their bubble compared to outside. However, all Cohen’s D were below 0.2, meaning there was no statistically significant difference between the ratings.

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="/assets/img/question2/neighbours_regions_cohend.html" 
            width="800" 
            height="500" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

## Custom region analysis
Next, we analyzed the regions we constructed earlier based on insights from the neighboring regions analysis of part 1 to see if we can see more trends. For these custom clusters, we compared in-region and out-region ratings using Cohen’s D. Again, all Cohen’s D values remained below 0.2, confirming that users did not rate beers from their own regions significantly higher.

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="/assets/img/question2/regional_on_question1.html" 
            width="800" 
            height="500" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

# 3) Looking at the state level, do we see more trends ? By doing a sentiment analysis do the text reviews reveal similar trends ? 

## Ratings analysis

![Mon image descriptive](/assets/img/question3/own_ratings_vs_other_ratings.png)

![Mon image descriptive](/assets/img/question3/cohensd_in_state_vs_out_state.png)

![Mon image descriptive](/assets/img/question3/ratings_distributions_average_ratings_high_cohensd.png)

## Sentiment analysis

![Mon image descriptive](/assets/img/question3/sentiment_analysis_reviews_local_vs_nonlocal.png)

![Mon image descriptive](/assets/img/question3/cramers_v_result.png)

# 4) Looking deeper into preferences, does separating by beer style reveal a style specific bias that could explain these differences in ratings?

![Mon image descriptive](/assets/img/question4/top_beer_style_high_norm_weight_per_state.png)

![Mon image descriptive](/assets/img/question4/percentage_share_beer_styles_by_users.png)

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="/assets/img/question4/dbscan_clustering_on_umap.html" 
            width="1000" 
            height="1200" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="/assets/img/question4/usa_state_cluster_based_on_dbscan.html" 
            width="1000" 
            height="1200" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

# 5) Going the other way around, if we cluster beers by beer attributes and ratings, do we see regional bias ?

<div>
  <style>
    iframe {
      width: 100%;
      height: 600px;
      border: none;
      margin-top: 20px;
    }
    .control-container {
      margin: 20px 0;
      text-align: center;
    }
    #k-slider {
      width: 300px;
    }
  </style>

  <!-- Dropdown Selector -->
  <div class="control-container">
    <label for="k-dropdown">Select k:</label>
    <select id="k-dropdown">
      <option value="3">k = 3</option>
      <option value="4">k = 4</option>
      <option value="5">k = 5</option>
      <option value="6">k = 6</option>
      <option value="7">k = 7</option>
      <option value="8">k = 8</option>
      <option value="9">k = 9</option>
      <option value="10">k = 10</option>
    </select>
  </div>

  <!-- Slider -->
  <div class="control-container">
    <label for="k-slider">Or use the slider:</label>
    <input id="k-slider" type="range" min="3" max="10" value="3" step="1">
    <span id="k-slider-value">3</span>
  </div>

  <!-- Frame to Display the HTML Files -->
  <iframe id="map-frame" src="assets/img/question5/clustering_by_beer_attributes_k3.html"></iframe>

  <script>
    const dropdown = document.getElementById('k-dropdown');
    const slider = document.getElementById('k-slider');
    const sliderValue = document.getElementById('k-slider-value');
    const iframe = document.getElementById('map-frame');

    // Function to update the iframe src
    function updateIframe(k) {
      iframe.src = `assets/img/question5/clustering_by_beer_attributes_k${k}.html`;
    }

    // Event listener for dropdown
    dropdown.addEventListener('change', (event) => {
      const k = event.target.value;
      slider.value = k;
      sliderValue.textContent = k;
      updateIframe(k);
    });

    // Event listener for slider
    slider.addEventListener('input', (event) => {
      const k = event.target.value;
      sliderValue.textContent = k;
      dropdown.value = k;
      updateIframe(k);
    });
  </script>
</div>
