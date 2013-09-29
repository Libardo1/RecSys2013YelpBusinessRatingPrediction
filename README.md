RecSys2013: Yelp Business Rating Prediction
---------------------------------------------

This repository contains 9th result (n_m) of RecSys 2013: Yelp Business Rating Prediction hosted by [kaggle][1]. All of the scripts are written in R. Here's the brief description of the model.

The model is based on glmnet in R exploiting sparse features derived from user and business information. Basically an ensemble of two models, with all features and with only user and business ids. As a post-processing, predicted review score is ensembled with user offset score, which is derived from user json file.

##Usage##
 - Specify your root directory in init.R as an absolute path. And also download data set from [kaggle][3] and put them in the raw directory.
The model also uses external name data from [US census][4]. You need to download dist.all.last, dist.male.first, and dist.female.first files and put them in data directory.

 - Call the scripts in the following order. The system requires 2~3 GByte of memory and takes about an hour to run all of the scripts.
   1. read.R
   2. preprocess.R
   3. extract_features.R
   4. submitter.R


###Note###
The result produced by the scripts in this repo is not exactly the same as n_m's rank (score: 1.23688) on the [private leaderboard][2], but almost the same, slightly better (score: 1.23669). The details of parameter settings during the competition are gone.

[1]: http://www.kaggle.com/c/yelp-recsys-2013
[2]: http://www.kaggle.com/c/yelp-recsys-2013/leaderboard
[3]: http://www.kaggle.com/c/yelp-recsys-2013/data
[4]: http://www.census.gov/genealogy/www/data/1990surnames/names_files.html