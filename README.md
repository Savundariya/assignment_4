# assignment_4
swiggy Restaurant Recommendation System using Streamlit 

This project is a **Restaurant Recommendation System** built using a real-world Swiggy dataset. It uses **machine learning clustering** (K-Means) and an interactive **Streamlit web app** to help users discover top-rated and cost-effective restaurants based on their preferences.

##  Project Overview

The goal of this project is to:
- Understand and clean the restaurant dataset
- Preprocess categorical and numerical features
- Use **K-Means clustering** to group similar restaurants
- Build an interactive **Streamlit app** that:
  - Takes user input (city, cuisine, rating, cost)
  - Finds matching restaurants
  - Recommends similar restaurants using clustering

---

##  Dataset

The dataset used (`raw_data.csv`) contains the following columns: ['id', 'name', 'city', 'rating', 'rating_count', 'cost', 'cuisine', 'lic_no', 'link', 'address', 'menu']

##  Project Structure

```text
Project4/
│
├── Project_4.ipynb              # Jupyter notebook with all preprocessing and modeling
├── streamlit.py                 # Final Streamlit app file
├── cleaned_data.csv             # Cleaned and filtered restaurant data
├── encoded_numeric.csv          # One-hot encoded and numeric-only dataset
├── kmeans_model.pkl             # Trained K-Means clustering model

## Step-by-Step Workflow
1. Data Understanding and Cleaning
Removed duplicates and missing values
Cleaned fields like cost and rating
Saved cleaned file as cleaned_data.csv

2. Data Preprocessing
Applied One-Hot Encoding to categorical fields like city and cuisine
Kept only numeric features
Saved as encoded_numeric.csv

3. Model Building
Used K-Means Clustering to cluster restaurants
Saved trained model as kmeans_model.pkl

4. Streamlit App
Built a UI to take user input (city, cuisine, rating, cost)
Filters restaurants using user preferences
Finds restaurants from the same cluster
Displays top 5 recommended restaurants with details

## Running the App
 Requirements
Install the dependencies:

python -m venv env
pip install streamli
pip install scikit-learn

## Run the Streamlit App
streamlit run streamlit.py
