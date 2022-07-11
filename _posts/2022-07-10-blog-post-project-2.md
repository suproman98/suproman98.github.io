
## Project Overview

This project consisted of exploratory analysis on the [Online News
Popularity](https://archive.ics.uci.edu/ml/datasets/online+news+popularity)
dataset. This data mainly focused on the number of `shares` (our
response) by `channel`. As there were six channels, we needed to
automate the code to subset and create documents based on each channel,
allowing the code to run each of the four models we created for each
channel. The dataset was quite large, consisting of a large number of
quantitative and categorical variables, which made model creation quite
difficult. We created summary statistics and various plots to visualize
the data, but we still could not tell which variables had strong
interactions with the response. However, the purpose of this project was
to investigate a few models and see how one model performs against the
rest. Our metric was `RMSE`, though we did not use the same number of
variables for each model, nor did we use the same variables. We simply
looked at which models performed better against others based on channel.

## Difficulties and Reflections

I wouldn’t necessarily do anything differently. Rather, I would want to
expand on the work done for this project. Different machine learning
methods and ensemble models could have yielded a better fit on the test
data, but if anything, I would want to dive deeper into model creation.
There are so many different ways to experiment with creating a good
model, and I did not utilize methods such as `bagging` or `glm` models
for instance, though they could output better results. I would want to
definitely look into the relationships between variables and how they
were correlated with each other or how strong their interactions were in
relation to `shares` before anything else. I think this project was
quite in-depth with how machine learning and regression models pertain
to various datasets, and as data gets more complex, there are more ways
to dive into model creation. Adding penalties to a linear model or using
different splits during cross validation could have yielded better
results. All in all, I think this was a difficult, yet interesting
project because of the vast number of models that could have been
created, but I think our methodology was a good base to expand on for
future projects.

## Takeaways

I addressed this a little bit in the previous section, but the biggest
takeaway for me was how extensive model selection/creation goes. There’s
never going to be “the perfect model” to test new data, but we can get
as close as we can to create models that take in data in real time.
Machine learning is an incredibly useful, in-depth, and quite frankly a
fun topic to get into, since you have to get creative with generating
equations or parameters to get better results. You won’t ever get the
perfect model, but you can definitely implement ways to try and get
close. Regardless, before getting into creating a regression or ensemble
model, it’s vital to examine your data, understand each variable, and do
extensive exploratory analysis (depending on the data complexity and how
deep you want to go) before you start creating any models.

## Links to Github Repo and Pages

-   [github repo](https://github.com/suproman98/project-2.git)
-   [github pages](https://suproman98.github.io/project-2/)
