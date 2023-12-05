# Video-Game-Recommender-AI

# How to Run

- Upload User data: follows format of the csv file
- simply run

# libraries

- scikit learn
- pandas
- matplot lib
- Pillow

# overview

Given Both User and Global Video Game Data
Preprocessing
- Converts 'tbd' values to NaN and numeric columns to numeric types.
- Drops rows with missing values in 'User_Score' and 'Critic_Score'.
- Standardizes the scores using StandardScaler.
Clusters
- Creates a new column 'Global_Score' as the average of 'User_Score' and 'Critic_Score'.
- Clusters based on Genre, assigning a unique color to each genre cluster
K Nearest Neighbor
- Takes into account all user data points, genre, and system finding the closest average Global Score in the global dataset
- Matches pick based on genre specification and how often specific genres appear
Output
- Displays a Tkinter messagebox with the recommended game based on the KNN clustering

# Limitations
Quality of User Input
- Without much data from a user, our system lacks the ability to make accurate predictions
- Example: users who provide their top three games for data will suffer generalized recommendations due to lack of KNN ability to draw comparisons
Assumption of Global Score
- Global Scores are assuming that games with the highest rating by users and sales will be the better games to be recommended to others
- Generally, these games are rated higher for good reason, although can fall short in unique cases
User Input Handling
- User data must be inputted in a specific column format, thus lots of data is needed to be collected from each user and game they enjoy
