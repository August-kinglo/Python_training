# PYTHON

# I- UNIVERSITY OF MICHIGAN : DATA STRUCTURES IN PYTHON

Certification obtained: https://coursera.org/verify/specialization/4T5YK4V7E5CD
# II- IBM DATA SCIENCE PROFESSIONAL CERTIFICATE

## 1. Data science methodology

## 2. Database manipulation 

## 3. Data analysis
### 3.1. Pandas
#### a. groupby 
- Pay attention when using more than two colums to groupby. It is wise to put as_index=False


### 3.1. Linear regression
The first step is to split the data into two groups.

msk = np.random.rand(len(df)) < 0.8
train = cdf[msk]
test = cdf[~msk]

The second step is to train the distribution

from sklearn import linear_model
regr = linear_model.LinearRegression()
train_x = np.asanyarray(train[['Variable_1']])
train_y = np.asanyarray(train[['Variable_2']])
regr.fit(train_x, train_y)

The coefficients
print ('Coefficients: ', regr.coef_)
print ('Intercept: ',regr.intercept_)

The third step is to plot the fitting line

plt.scatter(train.Variable_1, train.Variable_2,  color='blue')
plt.plot(train_x, regr.coef_[0][0]*train_x + regr.intercept_[0], '-r')
plt.xlabel("Variable_1")
plt.ylabel("Variable_2")

## 4. Data visualization 

### 4.1. Classic data visualization

#### a. Matplotlib and Seaborn 
#####  i. An Overview
Seaborn is built on top of Matplotlib. There are two ways to plot with those libraries. 
- Either by using pandas (df.plot(kind=type, x=, y=))
- Or by using directly the plt.type or sns.type
def style (style):
#The purpose of this function is to set the style of my graph directly
plt.style.use(style)

def plot_type (type):
#The purpose of this function is to set the type of plot I intend to plot directly
data.plot(kind=type)

More informations on : https://seaborn.pydata.org/ ; https://matplotlib.org/ 

### 4.2. Geospatial data visualization

### 4.3. Dasboards or interactive visualization
Web-based dashboarding : Plotly|Dash - Panel - Voilà - Streamlit
Plotting libraries : bokeh - ipywidgets - matplotlib - Bowtie - Flask

#### a. Plotly
#####  i. An Overview
- Interactive, open-source plotting library
- Supports over 40 unique chart types
- Includes various types of charts
- Visualizations can be :
    Displayed in Jupyter notebook and Saved to HTML files or being used in developing python-built web applications using [Dash]
- Useful link for Plotly : https://plotly.com/python/ and API Reference : https://plotly.com/python-api-reference/
##### ii. Command summary : two sub-modules
- plotly.graph_objects.figure propose a low-level interface to figures, traces and layout
  
- plotly.express propose a high-level interface
  
#### b. Dash 
#####  i. An Overview

- Open-source User Interface Python library from Plotty
- Easy to build GUI
- Declarative and Reactive
- Rendered in a web browser and can be deployed to servers
- Inherently cross-platform and mobile ready
- Useful link for Dash : https://dash.plotly.com/installation

##### ii. Command summary

## 4. Machine Learning technics
### 4.1 Major machine learning techniques

#### a. Regression/Estimation
Prediction continuous values. It can be performed through simple linear regression ou multiple linear regression approaches.
The accuracy of the model can be assessed by some metrics such as MSE, RMSE.

- Classification :
Predicting the item class/category of a case. It can be performed through - Decision trees, Naïve Bayes, Linear Discriminant Analysis, K-Nearest Neighbor, Logistic Regression, Neural Networks, Support Vector Machines (SVM).
The accuracy of the model can be assessed with some metrics such as F1score (1) based on the confusion matrix, Jaccard Index (1), Logloss (0).

- Clustering :
Finding the structure of data; summarization
- Associations :
Associating frequent co-occuring items/events
- Anomaly detection :
Discovering abnormal and unusual cases
- Sequence mining :
Predicting next events , click-stream (Markov Model, HMM)
- Dimension Reduction :
Reducing the size of data (PCA)
- Recommendations systems :
Recommending items
- Difference between atificial intelligence, machine learning, and deep learning :
      
AI components (computer vision, language processing, creativity) ; Machine learning (Classification, clustering, Neural Network); Revolution in ML (Deep learning)

## Projects
