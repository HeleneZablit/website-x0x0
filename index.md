---
layout: home
title: "Exploring Geographical Biais in Beer Taste in the US"
subtitle: "Is Your State Swaying Your Sip?"
cover-img: "/assets/img/background_test.png"
---
# Introduction

Beer, the most common alcoholic beverage. Grabbing a beer has become one of the world’s favorite pastimes. It is a chance to get together amongst friends, decompress with colleagues after work.
From America’s prohibition era to the current globalisation of the beer market, the choice of beer in a bar has never been so varied. The choice one makes when ordering a beer has never highlighted internal bias as much as now.

<div style="display: flex; justify-content: center; gap: 10px;">

<!-- First image -->

<div>
    <img src="{{ site.baseurl }}/assets/img/image_budweiser.jpg" alt="Image 1" style="width: 300px; height: auto;">
    <p style="text-align: center;"></p>
  </div>

<!-- Second image -->

<div>
    <img src="{{ site.baseurl }}/assets/img/we_want_beer.jpg" alt="Image 2" style="width: 300px; height: auto;">
    <p style="text-align: center;"></p>
  </div>

<!-- Third image -->

<div>
    <img src="{{ site.baseurl }}/assets/img/taste_the_high_country.jpg" alt="Image 3" style="width: 300px; height: auto;">
    <p style="text-align: center;"></p>
  </div>

</div>

The strong economic competition gives way to a cut-throat rivalry. Each brewery wants to sell more, be the best, especially if they sell beer in the same location. Can beers that come from far away compete with the regional preference people might have?

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/image4_intro.jpg"  alt="Description de l'image" style="max-width: 100%; height: auto;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      It’s a claim we hear all the time: regions boasting about having the “best” beer. But what if there’s more to it than just national pride? What if the state you call home influences how you taste beer? What if your national pride is ingrained in your beer preferences? In this investigation, we dive deep into the beer preferences of Americans.
    </p>
  </div>

</div>

This leads us to our research questions:
Our question at hand: Do people from different states have a bias for their own beers? To crack the case, we’ll begin by examining the geography of beer preferences through the lens of U.S. states. Inspired by the idea that people from certain regions of the world share similar food tastes, we’ll analyze regional beer preferences, comparing neighboring states and even the way different beer styles shape the ratings by state. Join us as we sift through the data to uncover hidden trends and discover the reasons behind these regional biases. Could the answers be hiding in plain sight? Let’s investigate and find out.

# The Data Used

<div style="display: flex; align-items: center;">

<!-- Text on the left -->

<div style="flex: 2; padding-right: 20px;">
    <h2></h2>
    <p>
      Why did we analyse US states you may ask. We had access to a large dataset from both the BeerAdvocate and RateBeer websites, but as we began our investigation, we found it more than sufficient to focus on the BeerAdvocate data. BeerAdvocate had a higher percentage of U.S.-based users compared to RateBeer, making it a more suitable dataset for our analysis, which was focused on a well-defined geographical region—the United States. <br>
      As seen in the graph below, U.S. states have not only a larger quantity of users, but also a greater number of local and non-local reviews, as well as more beers produced within each region. Here, we defined "local reviews" as those where the user’s region matched the beer’s region of origin.
    </p>
  </div>

<!-- Image on the right -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/image_data_used.jpg" alt="Description de l'image" style="max-width: 100%; height: 400px;">
  </div>

</div>

![Mon image descriptive]({{ site.baseurl }}/assets/img/question0/local_vs_non_local_reviews_by_country.png)

Having more data at our disposal allowed us to minimize the impact of anomalies or outliers. Since our goal was to capture state-level trends in beer reviews, the increased number of reviews enabled us to shift focus away from individual reviewer opinions and instead analyze the broader geographical patterns.

# 1) Do regions like the same kind of beer?

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question1/image_fun_q1.jpg"  alt="Description de l'image" style="max-width: 100%; height: 300px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      Not all states see eye to eye. Whether it's their neighbors or states on the opposite coast, preferences diverge in subtle but telling ways. So we asked ourselves, do neighbouring states rate their local beers similarly? <br>
      While we are interested in seeing how well states get along on beer taste, we start by dividing into "bubbles". A bubble is defined as a state and all its immediate neighbors. We're examining how the beer ratings within these bubbles might reveal patterns of connection (or lack thereof) between states.

    `</p>`

</div>

</div>

To find our answer, we focus on Cohen's d value, which tells us whether the difference in rating tendencies are statistically significant or not. Let us therefore regroup the states that align in their ratings.

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question1/custom_region.html" 
            width="2000" 
            height="700" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question1/image_fun_2_q1.jpg"  alt="Description de l'image" style="max-width: 100%; height: 200px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      The results are varied: proximity doesn’t always equate to similarity in ratings. States like Maryland, nestled on the East Coast, show a striking alignment in their beer reviews with nearby states. But Louisiana, sitting comfortably in the heart of the South, reveals a surprising connection to California, far from its borders, rather than to neighboring Mississippi. On the other hand it is Mississippi, who ever agrees with them?
    </p>
  </div>

</div>

This being said, we have looked if there was statistical significance between the ratings between each bubble. We are not giving up nonetheless, the search must go on!

# 2) Do we see significant differences between regions when comparing beer ratings?

<div style="display: flex; align-items: center;">

<!-- Text on the left -->

<div style="flex: 2; padding-right: 20px;">
    <h2></h2>
    <p>
      Hmm. How interesting! To further deepen our investigation we extended our analysis to compare beer ratings between regions. Here we are interested in detecting significant differences in how users from a state rate their beers brewed in their own state compared to out of state beers. To do so, we looked at 2 different regions for comparison.
    </p>
  </div>

<!-- Image on the right -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question2/image_fun_q2.jpg" alt="Description de l'image" style="max-width: 100%; height: auto;">
  </div>

</div>

## Neighboring bubbles analysis

We first examined whether users in each neighboring  bubble showed preferences for beers in their bubble compared to outside. However, all Cohen’s D were below 0.2, meaning there was no statistically significant difference between the ratings.

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question2/neighbours_regions_cohend.html" 
            width="800" 
            height="500" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

## Custom region analysis

Next, we analyzed the regions we constructed earlier based on insights from the neighboring regions analysis of part 1 to see if we can see more trends. For these custom clusters, we compared in-region and out-region ratings using Cohen’s D. Again, all Cohen’s D values remained below 0.2, confirming that users did not rate beers from their own regions significantly higher.

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question2/regional_on_question1.html" 
            width="800" 
            height="500" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

# 3) Looking at the state level, do we see more trends ? By doing a sentiment analysis do the text reviews reveal similar trends ?

## Ratings analysis

![Mon image descriptive]({{ site.baseurl }}/assets/img/question3/cohensd_in_state_vs_out_state.png)

![Mon image descriptive]({{ site.baseurl }}/assets/img/question3/ratings_distributions_average_ratings_high_cohensd.png)

## Sentiment analysis

![Mon image descriptive]({{ site.baseurl }}/assets/img/question3/sentiment_analysis_reviews_local_vs_nonlocal.png)

![Mon image descriptive]({{ site.baseurl }}/assets/img/question3/cramers_v_result.png)

# 4) Looking deeper into preferences, does separating by beer style reveal a style specific bias that could explain these differences in ratings?

![Mon image descriptive]({{ site.baseurl }}/assets/img/question4/top_beer_style_high_norm_weight_per_state.png)

![Mon image descriptive]({{ site.baseurl }}/assets/img/question4/percentage_share_beer_styles_by_users.png)

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question4/dbscan_clustering_on_umap.html" 
            width="1000" 
            height="1200" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question4/usa_state_cluster_based_on_dbscan.html" 
            width="1000" 
            height="1200" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

# 5) Going the other way around, if we cluster beers by beer attributes and ratings, do we see regional bias ?


<div class="control-container">
  <label for="k-slider">Or use the slider:</label>
  <input id="k-slider" type="range" min="3" max="10" value="3" step="1">
  <span id="k-slider-value">3</span>
</div>

<!-- Frame to Display the HTML Files -->

<iframe 
  id="map-frame" 
  src="{{ site.baseurl }}/assets/img/question5/clustering_by_beer_attributes_k3.html" 
  style="width: 100%; height: 600px; border: none;"
></iframe>

<script>
  const slider = document.getElementById('k-slider');
  const sliderValue = document.getElementById('k-slider-value');
  const iframe = document.getElementById('map-frame');

  // Function to update the iframe src
  function updateIframe(k) {
    iframe.src = `{{ site.baseurl }}/assets/img/question5/clustering_by_beer_attributes_k${k}.html`; // Update src dynamically
  }

  // Event listener for slider
  slider.addEventListener('input', (event) => {
    const k = event.target.value;
    sliderValue.textContent = k; // Update slider label
    updateIframe(k);
  });
</script>
