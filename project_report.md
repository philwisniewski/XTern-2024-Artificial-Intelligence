# Reflection and analysis of research process

## Distributions and Biases
- Many variables are strongly skewed in favor of a subset of features, such as Years being vastly overrepresented by years 2 and 3. Order (target variable) appears to be roughly evenly distributed.
- Lots of categorical features, which lends itself towards favoring specific machine learning models if data is not transformed (which for the case of this mini-project, was not)
- Images of distibutions and contingency tables can be found in /Graphs and Tables/
## Other potential uses for data
- Rather than predicting students orders, this data could potentially be used to predict the amount of money students are willing to spend, the amount of food (measured in calories) students are likely to want, or the average time students get lunch based on a multitude of factors. Furthermore, this data could potentially be generalized into a model that predicts a student's desired meal for more than just the 10 meals offered, based on predicting the students desired calories or price and using that to predict which meal they would select, allowing further expansion of our food truck businesses.

## Implications
### Ethical Implications 
- While it can sometimes be unethical to store data on subjects, the specific data collected in this study should not be considered unethical. There is no personal identifying information in the dataset (under the assumption that students can not be identified based on their year, major, or university alone). Additionally, this information is often public information that can be found online if the name and other identifying information of the student is known. 
- The potential ethical implications arise based on whether the students were told that their data would be collected and stored when they ordered. And, if not told directly, written somewhere before they submitted their information. 
### Business Outcome Implications
- Depending on how successful the model/guessers are, the company can avoid spending more money. At the same time however, the draw of a potential deal could result in getting more customers. Depending if the alure of the potential deal brings in more money than the company would lose from guessing incorrectly, it may be beneficial to not provide the deal.
### Technical Implications
- Some variable values lack data in comparison to other values in the same variable. For example, there are 640 physics majors, yet only 3 civil engineering majors. This can lead to overfitting and a lack of generalization depending on the major of the student. A potential solution would be grouping majors by college within their university, for example, by combining the different types of engineering majors together.
- While this is unlikely given the current scale of the data, depending on if the data is continuously updated and stored, storage and complexity of training models may increase.

## Modeling
### Process for picking model
- Many of the features used in this dataset are categorical variables, suggesting that a variant of random tree/forest classification may be useful.
- As there does not appear to be one or two features that are strongly correlated with specific order choices, random trees/forests also may be good when looking at a combination of features.
- Not only are random forest models very strong due to their ensemble nature, but they are also easy to train.
- Random forest model was compared to other types of ML models and outperformed them. It should be noted that k-nearest neighbors and support vector machine models do not perform well on categorical features, inhibiting their success.
- Random forest was slightly outperformed by decision tree classifier. Decision tree classifier was then selected as final model

## Final Thoughts and Considerations
- In order to determine if creating and implementing the artificial intelligence based model was worthwhile, I would suggest calculating the money saved from using the model. This would involve finding how much more money was made by offering the potential for the 10% discount compared to not offering the discount. I would also benchmark the model against guessing the most popular dish or the most expensive dish all the time, to determine if the model was actually helping. Looking at the distribution of orders, guessing randomly appears to give a 1 in 10 chance of getting the order correct. As the models all had accuracies higher than this, it is likely it would be beneficial to implement the model assuming all other criteria stated was met.
