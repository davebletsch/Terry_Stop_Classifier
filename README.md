# mod_5_project: Classification Modeling

# Terry Stop Classification: Arrest v. Non-Arrest

This model uses data collected by the city of Seattle regarding all Terry stops by police officers. A Terry stop is defined as any stop based on reasonable suspicion. This could be considered a traffic stop; however, this data looks at stops of pedestrians of the the type stop-and-frisk.

The goal of these models, was to predict if a Terry stop would result in the subject's arrest based on certain characteristics of the officer, of the subject, and of the situation.

Officer Demographics:
* age
* race
* gender

Subject Demographics:
* age
* perceived race
* perceived gender

Situational Characterisics:
* time of day
* whether or not the subject was frisked
* if the subject was frisked, what type of weapon was discovered

After a bit of feature engineering (grouping stops that occurred late at night, grouping stops that were made by young officers) 3 models were run to try to predict the outcome.

If we were to simply assume a stop would not end in an arrest, we would be correct about 77% of the time.

The 3 models that I ran:

- logistic regression
- K Nearest Neighbor 
- XGBoost

were only marginally better at making this prediction. In the best case scenario (XGBoost hypertuned with GridSearch), accuracy improved to 77.78% though precision greatly improved.

In conclusion, these models were not a good tool for predicting whether a Terry stop in Seattle would end in an arrest. I took this as a good result, in that one could presume that the Seattle Police Department was not exhibiting bias in their handling of these types of stops. 
