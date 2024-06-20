# Tourify Machine Learning Path

The dataset we use consists of 6 types of data:

1. Tourify_Article.csv - Contains articles about tourist attractions and culinary spots.
2. Tourify_Category.csv - Contains 6 categories that will be used.
3. Tourify_Image.csv - Contains additional photos for each tourist attraction and culinary spot.
4. Tourify_Place.csv - Contains information about tourist attractions and culinary spots in various cities in Indonesia.
5. dummy_user.csv - Contains information about user id, location, and age of user.
6. rating.csv - Contains user information, tourist attractions, culinary spots, and ratings to create a recommendation system based on ratings.

The features of the dataset are as follows:

1. *Tourify_Article.csv*
   - article_id: Contains the unique ID of the article.
   - article_url: Contains the link to the article.

2. *Tourify_Category.csv*
   - category_id: Contains the unique ID of the category.
   - category_name: Contains the name of the category, consisting of _Taman Nasional, Desa Wisata, Cagar Alam, Budaya, Bahari,_ and _Kuliner_.
     
3. *Tourify_Image.csv*
   - image_id: Contains the unique ID of the image.
   - url_image: Contains the link to the additional image.

4. *Tourify_Place.csv*
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

5. *dummy_user.csv*
   - user_id: Contains the unique ID of the user.
   - location: Contains the hometown of the user.
   - age: Contains the age of the user.

6. *rating.csv*
   - user_id: Contains the ID of the user (from dummy_user.csv).
   - tourism_id: Contains the ID of the tourist attraction and culinary spot rated by the user.
   - user_rating: Contains the rating given by the user to the tourism_id.
