### ***Project 2 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:**  
Great work on this assignment! You made great use of various pandas, matplotlib, and seaborn functionality. The only direct advice that I have is to keep on practicing and take note of some of the 'tricks' and best practices that you see in class. I recommend that you continue to play with Python (ideally by using pandas) to really expand your abilities when it comes to more advanced techniques.

**Some notes**  
* Regarding your analysis plan, that is a good idea for *exploratory data analysis*, but usually we are referring to an analysis plan with a complete model. What model would you use in this case if you were to rewrite this plan? 
* Try out the imputation technique next time! When you have missing values, you might not want to impute a value like 0. For example, you could actually by saying that there exists students out there with a 700 GRE, Prestige 1.0 school, that was admitted to grad school, but they have a 0.0 GPA. This only imputes 'bad' noise into our model. What you could do is impute something like the median or mean to retain the value without disturbing the underlying distribution too much.
