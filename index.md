---
layout: home
title: "Exploring Geographical Biais in Beer Taste in the US"
subtitle: "Is Your State Swaying Your Sip?"
cover-img: "/assets/img/background_test.png"
---

Beer, the most common alcoholic beverage. Grabbing a beer has become one of the world’s favorite pastimes. It is a chance to get together amongst friends or decompress with colleagues after work. Beer is popular worldwide, even in the far away lands of the United States of America, where the end of the Prohibition opened the floodgates for American breweries to expand, and where globalization has since diversified offerings even further. The choice one makes when ordering a beer has never highlighted internal bias as much as now.


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

The strong economic competition gives way to a cut-throat rivalry. Each brewery wants to sell more and be the best, especially if they sell beer in the same location. Can beers that come from far away compete with locals beers that are firmly anchored in their region?

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/image4_intro.jpg"  alt="Description de l'image" style="max-width: 100%; height: 200px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      It’s a claim we hear all the time: regions boasting about having the “best” beer. But what if there’s more to it than just national pride? What if the state you call home influences how you taste beer? What if your national pride is ingrained in your beer preferences? In this investigation, we dive deep into the beer preferences of Americans.
    </p>
  </div>

</div>

Our question at hand: Do reviewers have a positive bias for beers coming from their own state? To crack the case, we’ll begin by examining beer preferences throughout the U.S. Inspired by the idea that people from neighbouring regions of the world share similar food tastes, we’ll analyze regional beer preferences, comparing neighbouring states and even the way different beer styles shape the ratings by state. Join us as we sift through the data to uncover hidden trends and discover the reasons behind these regional biases. Could the answers be hiding in plain sight? Let’s investigate and find out.

# What to choose, where to look?

<div style="display: flex; align-items: center;">

<!-- Text on the left -->

<div style="flex: 2; padding-right: 20px;">
    <h2></h2>
    <p>
      Why did we analyse US states you may ask. We had access to a large dataset from both the Why did we analyse only the U.S. you may ask. A good detective knows what to look at and what to isolate in a sea of information. We had access to a large dataset from both the BeerAdvocate and RateBeer websites, but as we began our investigation, we found it more than sufficient to focus on the BeerAdvocate data. BeerAdvocate had a higher percentage of U.S.-based users compared to RateBeer, making it a more suitable dataset for our analysis, which was focused on a well-defined geographical region—the United States. Our focal lens is getting smaller… <br>
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

# Do neighbours share a taste for beer?

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question1/image_fun_q1.jpg"  alt="Description de l'image" style="max-width: 300px; height: 300px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      Not all states see eye to eye. Whether it's their neighbours or states on the opposite coast, preferences diverge in subtle but telling ways. So we asked ourselves, do neighbouring states rate their local beers similarly? <br>
      While we are interested in seeing how well states get along on beer taste, we’ll start by dividing the U.S. into "bubbles". A bubble is simply defined as a central state and all its immediate neighbours. So there are 50 bubbles, one for each state. We're trying to see if the way users rate beers within their bubbles could reveal patterns and connections (or a lack thereof) between neighbouring states.


    `</p>`

</div>

</div>

To find our answer, we are using statistical significance tests (Cohen’s D), a powerful tool to analyze differences between distributions. More specifically, we are looking at the difference of average beer ratings, between the states of a bubble. By grouping multiple bubbles with statistical similarities, we can obtain broader, customised regions based on beer preferences. This aggregation of bubbles, as in a beer glass, can be called foam: bubbles with similar properties aggregating at the top of the glass. You can take a look at the foam on the graph just below. 

<div style="display: flex; justify-content: center; margin: 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question1/custom_region.html" 
            width="2000" 
            height="600" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question1/image_fun_2_q1.jpg"  alt="Description de l'image" style="max-width: 100%; height: 300px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      The results are varied: proximity doesn’t always equate to similarity in ratings. States like Maryland, nestled on the East Coast, show a striking alignment in their beer reviews with nearby states. But Louisiana, sitting comfortably in the heart of the South, reveals a surprising connection to California, far from its borders, rather than to neighbouring Mississippi. So there’s something more to simply being neighbours that influences a user's beer preferences. We are not giving up so easily, the search must go on!
    </p>
  </div>

</div>

# Bubble vs Bubble, Foam vs Foam : are they really different?

<div style="display: flex; align-items: center;">

<!-- Text on the left -->

<div style="flex: 2; padding-right: 20px;">
    <h2></h2>
    <p>
      In the same way draft beer pours into our glasses on a Friday night, let’s pour ourselves into this investigation. So far we have compared states within a bubble to each other and were able to customize new regions (foam), but to deepen our investigation we can look at both how bubbles and our foams compare to the others. Maybe by taking a bigger picture view of things, we can find some interesting results. Should this be true, it would be a small breakthrough, a step towards identifying regional bias. 
    </p>
  </div>

<!-- Image on the right -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question2/image_fun_q2.jpg" alt="Description de l'image" style="max-width: 100%; height: auto;">
  </div>

</div>

## Neighbouring Bubbles Analysis

The graph below is showing us differences in beer ratings between bubbles. If we get a Cohen’s D above 0.2 we can say that it is statistically significant, however, none of the bubbles attain the 0.2 threshold. Our lead is a dead end, maybe finer details are being lost as we’re averaging over a whole bubble? 

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question2/neighbours_regions_cohend.html" 
            width="800" 
            height="500" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

## Foam Analysis

<div style="display: flex; align-items: center;">

<!-- Text on the left -->

<div style="flex: 2; padding-right: 20px;">
    <h2></h2>
    <p>
      Now let’s look at our foam, and see if by comparing them we see any differences. Since they are grouped based on preference, different groups might be quite different in terms of taste. <br>
      Will they show us a bias in the ratings or is everyone just a fair player in the beer rating business?
    </p>
  </div>

<!-- Image on the right -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question2/image_fun_q2_2.jpg" alt="Description de l'image" style="max-width: 100%; height: 200px;">
  </div>

</div>

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question2/regional_on_question1.html" 
            width="800" 
            height="500" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

Well… The latter appears to have prevailed once again. No group has shown a significant bias towards their own group.  Does this mean that all users have the same tendencies when it comes to reviewing beers from different states? We must dig deeper.

Since we don’t see much on a big scale, let's try a more granular approach and analyse differences once again on a state-by-state level, but this time across the whole country instead of just within bubbles and foams. 

# Zooming In: State-Level Bias

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question3/image_fun_q3.jpg"  alt="Description de l'image" style="max-width: 100%; height: 200px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      Let us roll up our sleeves, take a beer in each hand, and find new leads in this investigation! We want to compare each state with the rest of the United States, our goal being to find states that really love their local beer. If certain states are extremely biased towards their own beers, we will be a step further in isolating geographical bias!
    </p>
  </div>

</div>

## Ratings analysis


By comparing the ratings given by users from a state for beers in state compared to out of state, we can locate states in which users are guilty of giving positively biased reviews towards their own beers.

![Mon image descriptive]({{ site.baseurl }}/assets/img/question3/cohensd_in_state_vs_out_state.png)

Aha! This finer lens finally reveals a lead, indeed we can see some differences between states! There are multiple states with significant Cohen's D. This means that states do have preferences in their taste of beer.

![Mon image descriptive]({{ site.baseurl }}/assets/img/question3/ratings_distributions_average_ratings_high_cohensd.png)

<div style="display: flex; align-items: center;">

<!-- Text on the left -->

<div style="flex: 2; padding-right: 20px;">
    <h2></h2>
    <p>
      Looking at the actual difference in average rating, in red we can see that most states do indeed have a bias in their beers compared to when rating out of state beers. For more than 50% of the states, this bias is positively weighted towards their own beers. However in a turn of events there are 17 states where there is actually a preference for out of state beers.  By far, Missourians are guilty of rating their own beers more positively than beers from elsewhere in the US, are they the most loyal to their local beers? We have to reap the fruits our lead gave us, and dig deeper into what drives these differences. What is the secret behind Missouri beer, which has its inhabitants in a chokehold?
    </p>
  </div>

<!-- Image on the right -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question3/image_fun_2_q3.jpg" alt="Description de l'image" style="max-width: 100%; height: 300px;">
  </div>

</div>

## Sentiment analysis : A Textual Clue?

We know that there are states that have significant differences in the way they rate beers, when we look at the average rating. So, let's follow the trail and try to expand what we compare states on and look at textual data. Indeed we have vast amounts of textual data to analyze, with over 8 million different reviews for beer!  We can run this through a NLP pipeline, and perform a sentiment analysis on this data. With this we can say that an individual sentence is ‘positive’, ‘negative’ or ‘neutral’, with a score for how positive/negative it is. Ideally, we would like to see that the sentiment bias revealed by the written text reviews align with the state specific biases uncovered using the ratings distributions.

![Mon image descriptive]({{ site.baseurl }}/assets/img/question3/sentiment_analysis_reviews_local_vs_nonlocal.png)

Looking at the percentage of positive/negative/neutral sentences for each state, comparing local and non local reviews, the distributions between positive, neutral and negative reviews are pretty similar between all states. This is surprising, as we expected differences based on our earlier analysis of the ratings. Let's try some statistical tests to see if there are significant differences.

![Mon image descriptive]({{ site.baseurl }}/assets/img/question3/cramers_v_result.png)

We performed a chi2 test followed by a cramer’s V test (equivalent to cohen’s D but for categorical values), but as we can see, although the p-values are small for the chi2-test (likely due to large population size), the cramer’s V tells us that the effect size is negligible, thus there is no significant difference between the populations of locals and non locals! Maybe we can still find something if we analyze the specific scores of our sentences?

![Mon image descriptive]({{ site.baseurl }}/assets/img/question3/cohens_D_across_all_states.png)

Alas, the trail has gone cold. The effect size is quite small, thus there are again no significant differences between local and nonlocal reviews for a state.
In conclusion, much to our surprise, and contrary to analysis just based on average ratings, where we did find results, it seems that just analyzing the text reviews reveals no bias when it comes to local and nonlocal beers. A possible explanation for this is that people who leave text reviews are more likely to have a positive experience, so we’re sampling reviews that are mostly positive (indeed they are looking at the stacked barchart), giving us no meaningful difference for locals and on locals, as people who've had an average or negative experience won’t bother leaving a text review. 
Additionally, people who leave reviews actually have to think about what they're writing, they’re more thoughtful, so potentially less biased, compared to people who just leave a quick rating without thinking about it much.

Let's expand our search a little and investigate the other factors at play, notable beer styles, could they lead us to a satisfying conclusion?

# A style specific bias?

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question4/image_fun_q4.jpg"  alt="Description de l'image" style="max-width: 100%; height: 300px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      The analysis of state based style groupings began with a straightforward approach—analyzing beer style ratings to determine regional preferences across states. Yet, as we dug deeper and examined the number of reviews per style in each state, a pattern emerged: three styles were consistently the most reviewed across the country; the American IPA, Imperial IPA and Imperial Stout. This prevalence could be masking potential state-level trends that might otherwise have been visible. Looking solely at the average ratings didn’t reveal any significant regional preferences, prompting us to investigate further by introducing additional parameters.
    </p>
  </div>

</div>

![Mon image descriptive]({{ site.baseurl }}/assets/img/question4/top_beer_style_high_norm_weight_per_state.png)

<div style="display: flex; align-items: center;">

<!-- Text on the left -->

<div style="flex: 2; padding-right: 20px;">
    <h2></h2>
    <p>
      Even after applying various techniques to weigh ratings against the volume of reviews, and delving beyond just the top-ranked style, we still were unable to uncover substantial differences in beer preferences across states. <br>
      The percentage distribution of beer styles reviewed by state also revealed that the percentage shares for the most common beer styles were quite similar for all states and it was difficult to come up with specific groupings by style and state. 

    </p>
  </div>

<!-- Image on the right -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question4/image_fun_q4_2.jpg" alt="Description de l'image" style="max-width: 100%; height: 300px;">
  </div>

</div>

![Mon image descriptive]({{ site.baseurl }}/assets/img/question4/percentage_share_beer_styles_by_users.png)

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question4/image_fun_q4_3.jpg"  alt="Description de l'image" style="max-width: 100%; height: 200px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      <b>Clustering on Style</b> <br>
      This prompted us to explore clustering as a way to reveal which states were most similar to each other. Using features based on beer style—such as ratings, aroma, appearance, palate, and taste we are able to create a more complete picture of our data by considering more parameters than simply the average rating for each style.
    </p>
  </div>

</div>

Using UMAP to reduce our features into 3 dimensions and DBSCAN to cluster our states revealed distinct clusters.

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question4/dbscan_clustering_on_umap.html" 
            width="1000" 
            height="600" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

Then as we’ve done before we can use these clusters to build a map of the US, maybe this time we’ll see some geographical biases.

<div style="display: flex; justify-content: center; margin: 20px 0;">
    <iframe src="{{ site.baseurl }}/assets/img/question4/usa_state_cluster_based_on_dbscan.html" 
            width="1000" 
            height="600" 
            style="border: none;" 
            title="Interactive Plot: Regional Analysis">
    </iframe>
</div>

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question4/image_fun_q4_4.jpg"  alt="Description de l'image" style="max-width: 100%; height: 300px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      It’s interesting to see that although these clusters are quite clearly defined, geographically they do not seem to be grouped together in an intuitive way. However, notably the largest grouping seems to encapsulate western and midwestern states. We'll analyse the results of this map together with the other maps in a later part. <br>
      So far we’ve found some interesting results,but maybe we’re going about it the wrong way, what if we look at it from the opposite direction, what if we instead cluster beers by their attributes and ratings, and see if we can recover regional biases that way?

    </p>
  </div>

</div>

# Clustering: Finding Patterns in the Foam

<div style="display: flex; align-items: center;">

<!-- Text on the left -->

<div style="flex: 2; padding-right: 20px;">
    <h2></h2>
    <p>
      We embarked on a quest to uncover the hidden patterns behind beer attributes – the different parameters that breweries modify slightly to make their beer different from the others. Our investigation focused on clustering these attributes to reveal the geographical distribution of reviewers within each cluster. This would indicate that the geographical bias is ingrained in the beer attributes, given that there is no geographical information in the features we are training the algorithm on. The clues emerged through clustering, with the optimal parameters for k means pointing us to k = 5 or k = 6.
    </p>
  </div>

<!-- Image on the right -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/question5/image_fun_q5.jpg" alt="Description de l'image" style="max-width: 100%; height: 300px;">
  </div>

</div>

<div class="control-container">
  <label for="k-slider">Use the slider:</label>
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

The clustering showed us that people's preferences are geographically biased: those who have the same taste, often, are neighbours!  Additionally we can see that there are certain regions that always belong to the same cluster. Namely: Maine, New York, Pennsylvania and Virginia often belong to the same cluster. South Carolina, Georgia Mississippi, Tennessee, Arkansas and Arizona group together. Minnesota, Wisconsin, Illinois, Iowa and Michigan also cluster together. And finally, Montana, North and South Dakota, Wyoming and Idaho often belong to the same cluster.

From this modest clustering, we can say that there are 4 regions that are recurrent in this case:<br>
1) New England and the Mid-Atlantic <br>
2) Southeast and South central <br>
3) The Midwest <br>
4) Mountain States <br>

Now let us compare the results of this clustering with all the other maps we’ve made, maybe there are some similarities between them?

# Comparing clustering, are the different maps we’ve made similar to each other?

The mystery deepens as we lay out the US maps generated by our different region-grouping methods. From crafting “custom regions” using Cohen’s D to running two distinct clustering analyses with a variety of beer parameters, the story unfolds in unexpected ways. Each method paints a different picture, with groupings shifting depending on the tools and criteria used—suggesting that clear geographical divides in beer preferences might be more difficult to define than expected. <br>

Yet, the East Coast emerges as a repeat offender, with certain states consistently sticking together across all clustering methods. Could their distinct beer preferences be the clue that sets them apart? When we look at our style-based clusters we get larger clusters indicating that many states share the same beer style preferences, making it harder to tease apart state-specific preferences. This is especially evident in the large grouping of the central states which are part of cluster 0, which is not present when using our other clustering methods.

# So does your State *really* Sway Your Sip?

<div style="display: flex; align-items: center;">

<!-- Image on the left -->

<div style="flex: 1; text-align: center;">
    <img src="{{ site.baseurl }}/assets/img/image_conclusion.jpg"  alt="Description de l'image" style="max-width: 100%; height: 600px;">
  </div>

<!-- Text on the right -->

<div style="flex: 2; padding-left: 20px;">
    <h2></h2>
    <p>
      After having pieced together all our clues and leads, we have uncovered some intriguing patterns in beer preferences. States with similar beer tastes often clustered geographically, perhaps hinting at regional influence. However, when comparing ratings between different bubbles, the differences proved insignificant. Interestingly enough, when we focussed our investigation. Over half the states were guilty in showing a clear bias towards favouring their own beers, while a strange twist of events, 17 states showed biased ratings against their own beers to favour out of state beers. In the style analysis, the clustering based on beer style parameters did allow us to group the states by preferences but its variation in states grouped together compared to the clustering of reviews by different beer parameters suggests that trying to define a state simply by its beer preferences is a complex case. Overall, the differences in beer preferences by state weren’t as pronounced as expected and that your state isn’t swaying your sip as much as we initially expected. Perhaps a broader analysis on country wide differences would allow us to see; does your Passport Pick your Pint?
    </p>
  </div>

</div>