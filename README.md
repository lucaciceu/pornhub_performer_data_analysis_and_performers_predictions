# pornhub_performer_data_analysis_and_performers_predictions

**Short description:**

Final Project for the Ironhack Data Analyst course. Analysing Pornhub performer (pornstars and models) data: predicting video views, pornhub ranking and suggesting alternate/similar performers

Dataset at : https://www.kaggle.com/data/206700

Merged the two files (pornstars and models) in one file

Predicted:
- video views (used regressions and random forrest)
- pornhub ranking (with and without the pornstar/model built-in ranking)

Also in the archive (rec 1 and 2) is a project built with Flask / html /css where I implement the recommendation engine built in "suggest a pornstar" in a mini-site 
To run it, download the archive, open and run it with an ide like pycharm and have fun with it :)

**Long description:**

My purpose all along was to check if the position of porn performers in the listing view in Pornhub can be predicted and how. Turns out it can be done quite precisely using the built-in ranking (pornstar ranking and model ranking, respectively) but I wanted to see if that can be done without that.
I split the dataset into 4 parts (pornstars male and female, models male and female) - the results are similar but more accurate for some categorties (ex.: model - women)
Ended up putting 13 regression models in a loop and extracting the best one (used  GridSearchCV for hyper-parameter tunning on Random Forrest, as it turned out to be the top model)

I also wanted to predict video views (basically, the main user popularity metric) - turns out that can be predicted with a scary accuracy of 0.99

From there I build a performer recommender (actually, several versions, all using pairwise_distances, but with different meetrics and outcomes - some returned one alternative, the one I ended up choosing returns a list of 10). I Saved that in a pickel file and deployed it via Flask as a local app.

Once that was working, I also put it up on the internet via  pythonanywhere.com at https://lucaciceu.pythonanywhere.com/rec

Have fun, clear your browser history!


