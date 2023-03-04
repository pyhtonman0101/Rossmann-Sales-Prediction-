<h1 align="center"> Rossmann Sales Prediction </h1>

<p align="center"> </p>
<h2> :floppy_disk: Problem Statement and Project Description</h2>
<p>Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.
You are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.</p>

![Forecast-Sales-using-Machine-Learning-1024x683](https://img.freepik.com/free-vector/boost-sales-abstract-concept-illustration-promote-product-online-digital-marketing-strategy-sales-plan-boost-your-business-increase-sales-customer-engagement_335657-357.jpg)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :floppy_disk: Table of Content</h2>

  * Problem Statement and Project Description
  * Project Files Description
  * Goal
  * Dataset Information
  * Exploratory Data Analysis
  * Random Forest Model
  * Technologies Used
  
![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

 <h2> :floppy_disk: Project Files Description</h2>

<p>This project contains two executable file as follows:</p>
<h4>Executable Files:</h4>
<ul>
  <li><b>Rossmann Sales Prediction - Capstone Project.ipynb</b> - Google Collab notebook containing data summary, exploration, visualisations and modeling, model hyperparameter tuning, model performance, evaluation and conclusion.</li>
</ul>

<h4>Source Directory:</h4>
<ul>
  <li><b>Data & Resources link :</b> https://drive.google.com/drive/folders/1qnxqMxy8_gI-siwVhUaQOBW1QbM_07g0</li>
</ul>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :book: Goal:</h2>

The interest in a product continues to change occasionally. No business can work on its monetary growth without assessing client interest and future demand of items precisely. Sales forecasting refers to the process of estimating demand for or sales of a particular product over a specific period of time. This project involves solving a real-world business problem of sales forecasting and building up a machine learning model for the same.

Our goal here is to forecast the sales for six weeks for each store and find out the factors influencing it and recommend ways in order to improve the numbers.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :book: Dataset information:</h2>

Features in the dataset:
Most of the fields are self-explanatory. The following are descriptions for those that aren't.
* Id - an Id that represents a (Store, Date) duple within the test set
* Store - a unique Id for each store
* Sales - the turnover for any given day (this is what you are predicting)
* Customers - the number of customers on a given day
* Open - an indicator for whether the store was open: 0 = closed, 1 = open
* StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
* SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools
* StoreType - differentiates between 4 different store models: a, b, c, d
* Assortment - describes an assortment level: a = basic, b = extra, c = extended
* CompetitionDistance - distance in meters to the nearest competitor store
* CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
* Promo - indicates whether a store is running a promo on that day
* Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
* Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
* PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store
    
![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :chart_with_upwards_trend: Exploratory Data Analysis</h2>
<p>There were more sales on Monday, probably because shops generally remain closed on Sundays which had the lowest sales in a week. 
Store type B though being few in number had the highest sales average. The reasons include all three kinds of assortments specially assortment level b which is only available at type b stores and being open on sundays as well.
The outliers in the dataset showed justifiable behaviour. The outliers were either of store type b or had promotion going on which increased sales.</p>
<p>Store type B was open on all seven days of the week and had more sales than any other store type and promotion had a positive effect across all store types.<p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :book: Random Forest</h2>

<p>Random forest is a supervised learning algorithm. It creates a "forest" out of an ensemble of decision trees, which are commonly trained using the "bagging" method. The bagging method's basic premise is that combining different learning models improves the overall output.
Simply said, random forest combines many decision trees to produce a more accurate and stable prediction.

![1_Mb8awDiY9T6rsOjtNTRcIg](https://user-images.githubusercontent.com/67974590/214353597-e432ac1d-d4ec-4a93-846f-81dc2cf52f1e.png)


<p>Furthermore, the random forest classifier is efficient, can handle a large number of input variables, and provides correct predictions in most cases. It's a very strong tool that doesn't require any coding to implement.</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

 <h2> :book: XGB Regressor</h2>

<p>The XGB Regressor model is an implementation of the XGBoost algorithm, which is an optimized version of gradient boosting. It is particularly useful for large datasets and high dimensional data, and is often used in Kaggle competitions and other machine learning challenges. The XGB Regressor model uses decision tree ensembles as its base learners and is trained by minimizing the gradient of the loss function. It is a powerful model that can be used for both regression and classification tasks.
 
![Flow-chart-of-XGBoost](https://user-images.githubusercontent.com/67974590/214810912-9cda9c5a-e722-4aa3-b362-0dad63c6fe8b.png)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
 
<h2> :chart_with_upwards_trend: Results</h2>
<p>In this case, the Random Forest model has a Test_R2 score of 0.9527, which is 3.49% higher than the Decision Tree model's score of 0.920600. This suggests that the Random Forest model is able to make better predictions than the Decision Tree model.

On the other hand, the XGB Regressor Tuned model has a Test_R2 score of 0.955427, which is 0.29% higher than the Random Forest model's score of 0.9527. This suggests that the XGB Regressor Tuned model is able to make slightly better predictions than the Random Forest model. However, the difference is small and may not be significant for all use cases. Therefore, it would be necessary to analyze other performance metrics and evaluate the trade-offs between the different models to determine which one is best suited for a particular task.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :book: Technologies Used::</h2>

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://user-images.githubusercontent.com/32620288/139657460-40ef4562-76bd-43f5-bbca-47b6bd29863e.png" width=100>](https://numpy.org)    [<img target="_blank" src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Pandas_logo.svg/450px-Pandas_logo.svg.png" width=150>](https://pandas.pydata.org)  [<img target="_blank" src="https://seaborn.pydata.org/_static/logo-wide-lightbg.svg" width=150>](https://seaborn.pydata.org) [<img target="_blank" src="https://matplotlib.org/_static/logo2_compressed.svg" width=170>](https://matplotlib.org)   [<img target="_blank" src="https://user-images.githubusercontent.com/32620288/137518674-f36c5ad3-3d64-4c7a-a07c-53f247750394.png" width=170>](https://colab.research.google.com/)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :books: References</h2>
<ul>
  <li><p>Andrew Udell, 'Predicting E-Commerce Sales with Random Forest'. [Online].</p>
      <p>Available: https://towardsdatascience.com/predicting-e-commerce-sales-with-a-random-forest-regression-3f3c8783e49b</p>
  </li>
  <li><p>ChatGPT. [Online].</p>
      <p>Available: (https://chat.openai.com/chat)</p>
  </li>
  <li><p>Builtin.com, 'Random Forest'. [Online].</p>
      <p>Available: https://builtin.com/data-science/random-forest-algorithm</p>
  </li>
  <li><p>Machine Learning Mastery, 'Random Forest for Time Series Prediction'. [Online].</p>
      <p>Available: https://machinelearningmastery.com/random-forest-for-time-series-forecasting/</p>
  </li>
  
![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- CREDITS -->
<h2 id="credits"> :scroll: Credits</h2>

Mohd Zahid Ansari | Avid Learner | Data Scientist | Machine Learning Engineer | Deep Learning enthusiast

<p> <i> Contact me for Data Science Project Collaborations</i></p>


[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mohd-zahid-ansari-900850198/)
[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/pyhtonman0101)
