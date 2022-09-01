# RecSys
Recommender System 2021 challange - Polimi
## Overview
The application domain is TV programs recommendation.  
The datasets provided contains both interactions between users and TV shows, as well as features related to the shows.  
Each TV show (for instance, "The Big Bang Theory") can be composed by several episodes (for instance, episode 5, season 3). The goal of the recommender system is not recommend a specific episode, but to recommend the TV show.

## Goal
The goal is to recommend a list of 10 potentially relevant items for each user.

## Dataset
The datasets includes around 6.2M interactions, 13k users, 18k items (TV shows) and four feature categories: 8 genres, 213 channels, 113 subgenres and 358k events (episode ids). 
The training-test **split** is done via random holdout, 85% training, 15% test. 

### In detail

**data_train.csv** : Contains the training set, describing implicit preferences expressed by the users.  
row : identifier of the user  
col : identifier of the item  
data : "1" if the user interacted with the item  

**data_ICM_genre.csv** : Contains the genres of the items. TV shows (items) may have multiple genres. All genres are anonymized and described only by a numerical identifier.  
row : identifier of the item  
col : identifier of the genre  
data : "1" if the item is described by the genre  

**data_ICM_subgenre.csv** : Contains the subgenres of the items. TV shows (items) may have multiple subgenres. All subgenres are anonymized and described only by a numerical identifier.  
row : identifier of the item   
col : identifier of the subgenre   
data : "1" if the item is described by the subgenre  

**data_ICM_channel.csv** : Contains the channles of an item. TV shows (items) are broadcasted on one or more channels. All TV channles are anonymized and described only by a numerical identifier.  
The file is composed of 3 columns:
row : identifier of the item  
col : identifier of the TV channel  
data : "1" if the item has been broadcasted on that TV channel  

**data_ICM_event.csv** : Contains the episodes of an item. TV shows (items) might contain one or more episodes. All episodes are anonymized and described only by a numerical identifier.  
The file is composed of 3 columns:  
row : identifier of the item  
col : identifier of the episode  
data : "1" if the episode belongs to the item  

**data_target_users_test.csv** : Contains the ids of the users that should appear in your submission file. The submission file should contain all and only these users.  

**sample_submission.csv** : A sample submission file in the correct format: [user_id],[ordered list of recommended items]. Be careful with the spaces and be sure to recommend the correct number of items to every user. 
