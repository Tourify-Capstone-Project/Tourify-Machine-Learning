# Tourify Machine Learning Path

## Data Information
The dataset we use consists of 6 types of data:

1. Tourify_Article.csv - Contains articles about tourist attractions and culinary spots.
2. Tourify_Category.csv - Contains 6 categories that will be used.
3. Tourify_Image.csv - Contains additional photos for each tourist attraction and culinary spot.
4. Tourify_Place.csv - Contains information about tourist attractions and culinary spots in various cities in Indonesia.
5. dummy_user.csv - Contains information about user id, location, and age of user.
6. rating.csv - Contains user information, tourist attractions, culinary spots, and ratings to create a recommendation system based on ratings.

The features of the dataset are as follows:

1. Tourify_Article.csv
   - article_id: Contains the unique ID of the article.
   - article_url: Contains the link to the article.

2. Tourify_Category.csv
   - category_id: Contains the unique ID of the category.
   - category_name: Contains the name of the category, consisting of _Taman Nasional, Desa Wisata, Cagar Alam, Budaya, Bahari,_ and _Kuliner_.
     
3. Tourify_Image.csv
   - image_id: Contains the unique ID of the image.
   - url_image: Contains the link to the additional image.

4. Tourify_Place.csv
   - tourism_id: Contains the unique ID of the tourist attraction and culinary spot.
   - tourism_name: Contains the name of the tourist attraction and culinary spot.
   - tourism_description: Contains the description of each tourist attraction and culinary spot.
   - category: Contains the unique ID of the category for each tourist attraction and culinary spot.
   - city: Contains the city of each tourist attraction and culinary spot.
   - price: Contains the highest price of each tourist attraction and culinary spot.
   - rating: Contains the average rating of each tourist attraction and culinary spot.
   - tourism_location: Contains the address of each tourist attraction and culinary spot.
   - tourism_image: Contains the main image of each tourist attraction and culinary spot.
   - latlong: Contains the latitude and longitude of each tourist attraction and culinary spot.
   - latitude: Contains the latitude of each tourist attraction and culinary spot.
   - longitude: Contains the longitude of each tourist attraction and culinary spot.

5. dummy_user.csv
   - user_id: Contains the unique ID of the user.
   - location: Contains the hometown of the user.
   - age: Contains the age of the user.

6. rating.csv
   - user_id: Contains the ID of the user (from dummy_user.csv).
   - tourism_id: Contains the ID of the tourist attraction and culinary spot rated by the user.
   - user_rating: Contains the rating given by the user to the tourism_id.
  
## Data Preparation
The following are some of the steps taken to prepare the data:
1. Data Preprocessing
    - Cleaning up duplication data.
        This is done because it can cause the same data to appear 2 or more times in the recommendation system that will be made. Therefore, this duplication data needs to be removed because the data actually already exists in the dataset.
2. Data Preparation
    - Encoding place and user labels 
        This is done to encode identifiers for places and users.
    - Mapping encoded place and user labels to rating data
        After the identifier is created, the results are entered into the tourism_rating.csv (rating) data in preparation for entering the modeling stage.

## Modeling and Result

## Evaluation
To measure the performance of our model for recommendation systems, the RMSE metric is used, which predicts normalized Place_Ratings based on encoded user_id and tourism_id.

RMSE is calculated by squaring the error (predicted - observed) divided by the amount of data (= average), and then rooted. Mathematically, the formula is written as follows

![image](https://github.com/Tourify-Capstone-Project/Tourify-Machine-Learning/assets/170117238/45d1c530-8e3b-4a0c-a5b0-c597ce97aaf7)

The advantage of RMSE is that it has a fairly high level of sensitivity, and RMSE also avoids the use of taking absolute values, which is undesirable in many mathematical calculations.

The RMSE in this collaborative filtering model is around 0.3, of course this is considered sufficient to be able to display the most appropriate recommendation results.
