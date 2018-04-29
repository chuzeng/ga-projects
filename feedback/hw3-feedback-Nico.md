### ***Project 3 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:**  
Fantastic job on this assignment! You nailed the entire process end-to-end. Killer job on the feature engineering. I am sure you did a bit of research online for how to best extract features on this dataset, but I hope you learned how creative you can be, and what it really means to extract features from data. Awesome! I put some notes below for some thoughts/improvements.

**Please let me know if any of these comments are unclear or if you have any questions at all! My goal is to provide you with effective feedback so that you get the most out of these assignments, so let me know if something doesn't sit right with you.**

**Some notes**  

* **Plotting**  When plotting with lots of features, I recommend that you take a look at just a subset of features. In particular, I would choose features of interest to be plotted by themselves and with your **target** variable. If you plot too much, you end up with an unreadable mess.
* **Using all your features**  You built tons of awesome features, but you only used a handful of them! Throw them all in there! Those features that you built will give huge amounts of lift for your model! Try re-running this but throw in some of those other columns that you engineered!
* **Hyperparameter optimization**  As we discussed in our review session, once you have decided on a solid set of features, you want to do some level of hyper parameter tuning. You currently aren't adding any penalty to your model, which could help with some over-fitting.
    - Logistic regression:
        - C : Amount of penalty you apply to your weights! Remember that in this implementation, it is actually 1/C. Thus, a smaller C means more penalty as you are adding MORE of the weights to the penalty.
        - penalty: 'l1' vs. 'l2'
        - fit_intercept : (this is a parameter, but you likely always use this term)
        - solver : {‘newton-cg’, ‘lbfgs’, ‘liblinear’, ‘sag’, ‘saga’} this is your term to change the optimization procedure! These can be interesting to experiment with. On a smaller dataset, this may not be so important, but when datasets become huge... This is very important.
    - KNN:
        - n_neighbors : Number of neighbors
* **Using different models**  So, why would you want to use LogisticRegression vs. KNN? Here are some pointers:
    - **Model structure**  Logistic regression is modeling the probability of a class occurring, given some data, to make a linear classification boundary. KNN does not have a model form, it is just empirically taking the structure of your training data and hoping that there is some local information given your data that will have once class be closer to another class (distance).
    - **Model output**  Logistic regression output model probabilities. This means that we can rank the outcomes of things (based on probability) and we can see a band of different outcomes! You have more information in there. When you use KNN, we are just applying a label to a new datapoint.
    - **Efficiency and performance**  If you have tons of features, KNN is going to be SLOW. At times, it will even be totally useless as distance becomes meaningless in high dimensions. Logistic Regression are very, very fast.
* **Scaling**  Remember that scaling can be very important for some models. In the case of KNN, it is very important that we scale because KNN is based on distance. Distance calculations are much more efficient, and telling, if you scale your data such that things are grouped together in a much more sensible fashion.
