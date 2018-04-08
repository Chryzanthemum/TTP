# Trust The Process
A project we threw together for
https://www.kaggle.com/c/mens-machine-learning-competition-2018

Basically the goal was to model every possible matchup in the NCAA March Madness tournament and predict a winner with a given degree of certainty. The more certain you were about an incorrect result, the more you were penalized. Overall, our team placed like 517/934 which is whatever, but not bad given how little we actually knew about the process/competition. 

Our biggest mistake was probably overbuilding our model. There was a decent degree of multicollinearity among our features, which I think XGBoost would have taken care of if we had allowed it to build deeper models, but we limited it to try and avoid overfitting due to the small pool of possible predictions. Some of the top teams used pure linear regression, I'd have to do more internal digging to see why that outperformed us.

The one advantage we did have over other teams was we didn't manually set any predictions. A common strategy used is to set all the 1 vs 16 games to a 100% chance of the 1st seed winning, which seriously hurt some teams this year. I mean, we still got it wrong, but we got it less wrong, ya feel?

Credits to @sunotsue (Su Park), @stillmatic (Christopher Hua)
