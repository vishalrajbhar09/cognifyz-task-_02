# cognifyz-task-_02




Restaurant Recommendation System using Python

This program builds a restaurant recommendation system that suggests restaurants to users based on their preferences. The program uses Cuisines and Price Range to generate recommendations with the help of TF-IDF Vectorization and Cosine Similarity. 

Program Explanation:- 

Step 1: Load the Dataset fro the task given CSV file
The dataset containing restaurant details is loaded from a CSV file.
You can preview the first few rows of the dataset using the head() function to understand its structure.

Step 2: Preprocess the Dataset
Missing Data Handling: Missing values in the Cuisines column are replaced with the word 'Unknown'.
Feature Combination: A new column, Combined_Features, is created by merging two columns:
Cuisines (e.g., Indian, Italian, etc.)
Price Range (e.g., 1, 2, etc.)
This combined column is used as input for building the recommendation system.

Step 3: Encode Text Data
The program uses TF-IDF Vectorization to convert textual data (Cuisines + Price Range) into numerical vectors.
TF-IDF stands for Term Frequency-Inverse Document Frequency and is a common technique for representing text data numerically.
This numerical matrix (called the TF-IDF matrix) is the input for comparing user preferences with restaurant data.

Step 4: Recommendation System
The program uses Cosine Similarity to find how similar a user's preferences are to the restaurants in the dataset.

The steps include:
Taking the user's input (e.g., preferred cuisine and price range).
Converting it into the same vector format as the dataset using TF-IDF.
Comparing this vector to all restaurants in the dataset using Cosine Similarity.
Sorting the restaurants by similarity and selecting the top 10 matches.

Step 5: Testing the Recommendation System
A sample user preference is defined (e.g., "Italian 2", meaning "Italian cuisine and Price Range 2").
The program generates recommendations for the sample input and displays the names of the top matching restaurants.
Output Example
Here’s how the program works when tested with a sample preference (Italian 2):

User Preferences: Italian cuisine and Price Range 2.
Recommended Restaurants:
Restaurant A
Restaurant B
Restaurant C
(...and so on, up to 10 restaurants)

after all this how you can use tbis program is below.

Dataset:first  Prepare a CSV file containing at least these columns:

Restaurant Name
Cuisines
Price Range
(Make sure to adjust the column names in the code if your dataset has different names.)

Then, Install Required Libraries:

pandas, scikit-learn, and numpy. You can install them using pip install pandas scikit-learn numpy.
Run the Program:

Update the file path of your dataset in the code:
python
Copy code
file_path = r'C:\path\to\your\dataset.csv'  (# the csv file provided by the task)
Define your user preferences (e.g., "vishal 3") and run the script to get recommendations.
Key Concepts Used
TF-IDF Vectorization: Converts text data into numerical values based on word importance.
Cosine Similarity: Measures how similar two vectors (numerical representations of text) are.
Recommendation System: Suggests restaurants based on the user’s preferences.
