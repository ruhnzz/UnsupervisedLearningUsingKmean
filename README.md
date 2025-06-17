# UnsupervisedLearningUsingKmean
statement: Scenario - You are working for an automotive company, and your task is to cluster vehicles into groups based on their features such as weight, engine size, and horsepower.

pandas is a powerful Python library used for data manipulation and analysis.
numpy is used for numerical operations.
pyplot is a sub-library of matplotlib ,This is used for data visualization.
from sklearn.cluster import KMeans =>This imports the KMeans clustering algorithm from scikit-learn, a popular machine learning library.
KMeans is an unsupervised learning technique that groups data into k clusters based on feature similarity.

warnings.filterwarnings('ignore') => ignores the warning messages and keeps the code clean

np.random.seed(0) => we use seed to fix the random numbers to be same whenever they generated 

np.random.randint(low,high,size) => to get random interger values
np.random.uniformt(low,high,size) => to get random floating point values

df = pd.DataFrame(data) =>Convert the dictionary data into a pandas DataFrame(table) called df.

X = df => storuing table in X ,X represents your input data that will be passed to the clustering model.

kmeans = KMeans(n_clusters=3, random_state=42) => defining model
n_clusters=3: You want the algorithm to group the vehicles into 3 clusters. we can change as per requirement
random_state=42: Fixes the randomness so the clustering result is reproducible every time you run it.

kmeans.fit(X) => training the model

plt.scatter(df['Weight'], df['Horsepower'], c=kmeans.labels_)
This line draws a scatter plot of two features: Weight (x-axis) and Horsepower (y-axis).
kmeans.labels_ is a NumPy array of size 300
It contains the cluster number (0, 1, or 2) for each vehicle.
Group the data into 3 clusters based on their similarity it assingins each cehicle to be 0 0r 1 0r 2 cluster number






