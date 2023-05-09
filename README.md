# movie-recommender-with-SVD
The system will be designed to recommend movies to users based on their past movie ratings and will be trained on a dataset of movie ratings. The system will not involve the creation of a user interface, but rather focus on the development of the recommendation algorithm. The evaluation of the system will be based on standard evaluation metrics for recommender systems such as Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
3.1 Data Collection Techniques
The dataset used in this project was obtained from the Kaggle website. It is a collection of user ratings for different movies, along with metadata such as movie titles, genres, release years and User_Id. The dataset contains 25m ratings from 162k users on 25kmovies. 

3.2 Data Pre-processing Methods
To prepare the data for analysis, we transformed the data into a matrix format, the genres to become individual columns of their own and gave them indicators of 1 and 0, in which genres that belong to a certain movie are given 1 while if not 0 is assigned.

3.3 Feature Extraction and Selection Techniques
In order to reduce the dimensionality of the data and improve computational efficiency, we used Singular Value Decomposition (SVD) to extract the most important features from the rating matrix. We selected the features, based on their contribution to the overall variance of the data.

3.4.1 Model Development Requirements
The model was developed using Python 3.7, with the following packages: NumPy, Pandas, and Scikit-learn. The code was run on a standard laptop with 8GB RAM and a 2.4GHz Intel Core i3 processor.

3.4.2 Model Development Algorithm
We used a collaborative filtering approach, specifically matrix factorization with SVD, to develop the recommender system. This method works by decomposing the rating matrix into two lower-dimensional matrices, one for users and one for movies. These matrices are then used to predict missing ratings and generate recommendations.

3.4.3 Training and Optimization
To train the model, we used the SVD algorithm to factorize the rating matrix into its user and movie components. We then used these components to reconstruct the original matrix and calculate the prediction error. We optimized the model by adjusting the number of latent factors and the regularization parameter, using grid search and cross-validation techniques. The final model achieved an RMSE of 0.84  on the test set, indicating good predictive performance.
