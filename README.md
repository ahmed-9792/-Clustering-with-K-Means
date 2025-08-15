Clustering with K-Means:

 📌 Objective
The goal of this task is to perform unsupervised learning using the K-Means clustering algorithm to group customers into distinct clusters based on their annual income and spending score.

 🛠 Tools & Libraries
- Python 3
- Pandas – Data loading & preprocessing
- Matplotlib – Data visualization
- Scikit-learn – K-Means clustering, StandardScaler, Silhouette Score

 📂 Dataset
Dataset: 'Mall_Customers.csv'  
This dataset contains customer demographic and spending data, including:
- CustomerID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1–100)

 Example Rows:
| CustomerID | Gender | Age | Annual Income (k$) | Spending Score (1-100) |
|------------|--------|-----|--------------------|------------------------|
| 0001       | Male   | 19  | 15                 | 39                     |
| 0002       | Male   | 21  | 15                 | 81                     |
| 0003       | Female | 20  | 16                 | 6                      |

📋 Steps Performed
1. Load and inspect the dataset
2. Data cleaning:
   - Removed duplicates
   - Handled missing values
   - Standardized column names
3. Feature selection:
   - Selected 'Annual Income (k$)' and 'Spending Score (1-100)' for clustering
4. Feature scaling:
   - Standardized features using 'StandardScaler'
5. Finding optimal clusters:
   - Used Elbow Method to find the point where inertia reduction slows
   - Used Silhouette Score to measure cluster quality
6. Model training:
   - Fitted K-Means with optimal 'K'
7. Evaluation:
   - Calculated final Silhouette Score
8. Visualization:
   - Plotted clusters with color-coding
   - Marked centroids

📊 Results
- Optimal K was chosen based on maximum silhouette score
- Final Silhouette Score: '~0.55' (may vary depending on dataset)
- Clear grouping of customers into segments (e.g., high income–low spending, low income–high spending)

 🚀 How to Run
1. Install required packages:
   pip install pandas matplotlib scikit-learn
Place Mall_Customers.csv in the same folder as the script or notebook.

Run the notebook:
jupyter notebook TASK8.ipynb
Or run the Python script version:
python task8_kmeans.py

📌 Notes
n_init='auto' is used in KMeans to remove future warnings from scikit-learn.

On Windows with MKL, a known memory leak warning is avoided by setting:
import os
os.environ["OMP_NUM_THREADS"] = "1"
