# MOVIE-RECOMMENDATION-SYSTEM

# 1. BUSINESS UNDERSTANDING
### Problem Statement
Streaming platforms such as Netflix, Disney+, Amazon prime among others face a challenge: Users are overwhelmed by thousands of movie choices.

The objective is to develop an intelligent recommendation system, that is capable of predicting movies that a user is likely to enjoy based on:

- Historical ratings
- Movie genres
- User preferences
- Similar users and movies

## Business objectives
Build a Recommendation system that:

= Improves user engagement
- Personalizes user experience
- Increases watch time
- Reduces search effort

## Success Criteria
The recommendation system will be considered successful if it achieves low RMSE and MAE values while maintaining high Precision@10 and Recall@10 scores.

## 2. EXPLORATORY DATA ANALYSIS(EDA)

Here we show the relationship between:

- Ratings distributions
- top 20 most rated movies
- Ratings per user
- Top user leaderboard
- Top genres by average ratings
- Movie genre distribution
- Wordcloud of tags
- User activity distribution
- Rating timeline trends
- Movie popularity vs rating
- Correlation Heatmap


## 3. DATA PREPERATION

Here we cover:

- Creating Popularity metrics
- Weighted Rating
- User-Item Matrix Sparcity


## 4. MODELLING

There are several models used here in trying to find the best model for a recommendation system.
They include:

- Model 1: Popularity based Recommendation
- Model 2: Content-Based Filtering(TF-IDF)
- Model 3: User-Based Collaborative Filtering
- Model 4: Item-Based Collaborative Filtering
- Model 5: Matrix Factorization (SVD)


## 5. EVALUATION

Various evaluation methods were used, which include:

- Step 1: RMSE Comparison
- STEP 2: MAE COMPARISON
- STEP 3: PRECISION@K
- STEP 4: RECALL@K
- STEP 5: COVERAGE
- Step 6: Dashboard

Although user-based collaborative filtering achieved the highest precision@10, SVD achieved the lowest RMSE and MAE values while maintaining strong recommendation relevance. Therefore SVD provides the best balance between rating and prediction accuracy and recommendation quality and is selected as the final deployment model.

## 6. DEPLOYMENT

The system:

Receives User ID
Identifies unseen movies
Predicts ratings
Ranks movies
Returns Top 10
This simulates real-world recommendation deployment.

## CONCLUSION

- EDA revealed that user ratings are generally positive, with most ratings concentrated between 3 and 5 stars.
User-item interaction matrix was highly sparse, indicating that users rate only a small fraction of the available movies, which is a common challenge in recommendation systems.
- Popularity-based recommendations provide simple recommendations based on highly rated and frequently rated movies but lacked personalization.
Content-based filtering successfully recommended movies with similar genres but was limited with available movie metadata.
- User-based and Item-based collaborative filtering leveraged historical rating behaviour to generate personalized recommendations.
- SVD achieved the best prediction performance with an RMSE of 0.88 and MAE of 0.67, indicating the lowest prediction errors among evaluated models.
- User-based collaborative filtering achieved higher precision@10 (0.65) demonstrating strong recommendation quality.
Based on overall evaluation resaults, SVD was selected as the most suitable recommendation model for deployment.


## 8. RECOMMENDATIONS

- Deploy the SVD recommendation model as the primary recommendation engine because it achieved the best overall performance across RMSE,MAE,Precision@10 and Recall.
- Develop a hybrid recommendation system that combines SVD and Content-based filtering to improve recommendation quality.
- Periodically retrain the recommendation model using newly collected rating to ensure recommendations remain relevant and adapt to changing user preference.
