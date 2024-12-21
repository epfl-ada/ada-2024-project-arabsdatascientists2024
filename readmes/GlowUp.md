<br><br>
So Astra, the data has spoken, and using linear regression we can reveal the perfect formula for your Hollywood glow-up.<br><br>

While being too attractive could actually hurt your score, forget about arched eyebrows too. However, the public seems to have a soft spot for gray hair, which could also simply be related to being a more experienced actor.<br><br>

Moving on to your vibe: bags under the eyes, is apparently “in”. So don’t sleep too much, it’s your secret weapon! rosy cheeks and sweats? Not the public’s vibe. And big lips? Also a no-go. <br><br>

This graph illustrates the coefficients of significant features in a regression model, with the blue dots representing coefficient values and red bars showing their confidence intervals. Features whose confidence intervals exclude zero (e.g., C(Male)[T.1] and C(Gray_Hair)[T.1]) are statistically significant, indicating a meaningful positive or negative effect on the dependent variable, while those crossing zero (e.g., C(Bags_Under_Eyes)[T.1]) are not significant.<br><br>

<div style="text-align: center;">
  <img src="assets/media/graphlylia.png" alt="graphlylia" class="physique-graphlylia">
</div>

<style>
.physique-graphlylia {
  max-width: 50%; 
  height: auto;   
}
</style>
<br><br>

There are some power duos in the physical attribute game that push you straight to the top of the rankings. We used saturated regression for pairs of features, which involves fitting a model where all possible interactions and combinations between two features are included as parameters. <br><br>

First up, pale skin paired with rosy cheeks: the ultimate clean skin vibe. And how could we not mention the timeless combo of mysterious dark hair and irresistible attractiveness? Unfortunately, not every combo makes the cut. The “I’m attractive, but my bags under the eyes prove I’m only human” vibe? Turns out it’s not part of the secret success formula. <br><br>

Features whose intervals exclude zero (e.g., C(Pale_Skin)[T.1]:C(Rosy_Cheeks)[T.1]) are statistically significant, indicating positive or negative effects on the dependent variable, while those crossing zero are not significant.


<div style="text-align: center;">
  <img src="assets/media/graphlylia2.png" alt="graphlylia2" class="physique-graphlylia2">
</div>

<style>
.physique-graphlylia2 {
  max-width: 50%; 
  height: auto;   
}
</style>
<br><br>

Further analysis revealed another critical factor: height. The boxplot below highlighting the height distribution by KMeans clusters and gender: <br><br>

<div style="text-align: center;">
  <img src="assets/media/genderandheights.png" alt="genderandheights" class="physique-genderandheights">
</div>

<style>
.physique-genderandheights {
  max-width: 50%; 
  height: auto;   
}
</style>
<br><br>

We started by clustering our data according to all the features we have. Since our data is cathegorical, we used hot encoding in order to use K-means model which is more adapted in our case, and according to our data - that had levels for example for education or priviledge. 

We gained an additional insight: successful women tend to be taller than average, while less successful men are shorter than average. In simpler terms, being tall for a man is almost a baseline requirement for success. It doesn't provide an extra advantage, but not meeting this baseline can be a disadvantage. This finding reflects deeply ingrained societal biases in how physical traits influence perceptions of leadership and prominence.<br><br>

"Astra," we said after sharing these findings, "your journey highlights how deeply societal expectations are intertwined with success. You will embody the strength and charisma expected of male actors, but together, we aim to challenge these norms and create new standards for what it means to be successful”. <br><br>

"Astra," we said, "before we shape your path, let us share another key insight we've uncovered. Age and the timing of your career start plays pivotal roles in an actor's trajectory. We want you to be aware of that, so take a look on the careers of the most influential actors on your own."<br><br>


<iframe src="assets/interactive/age_distribution.html" class="interactive-career"></iframe>

*Astra looking at us confused*<br><br>

“ Here is a regression for you to see a bit clearer "
<br><br>

<div style="text-align: center;">
  <img src="assets/media/reg_careerstart.jpg" alt="regcareerstart" class="physique-regcareerstart">
</div>

<style>
.physique-regcareerstart {
  max-width: 50%; 
  height: auto;   
}
</style>
<br><br>

*Astra still looking confused* <br><br>

" Well, you surely won't be the smartest actor but you will be the most successful " <br><br>

This regression shows a negative correlation between career start age and success as the slope of the line is negative, suggesting that starting a career earlier is generally associated with higher success. However, the wide spread of data points indicates that career start age alone does not strongly predict success, as other factors likely play a significant role, which is the whole point of our analysis. <br><br>
