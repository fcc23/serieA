# **Machine learning analysis of football data ( Serie A )**

- **Order of Codes**

1. **Web Scraping from fbref.com**
   - In the first code, I performed web scraping from the [fbref.com](https://fbref.com/it/) website.
   - Using BeautifulSoup, I assembled the DataFrame `matches_21_24.csv`.
   - Extracted relevant statistics based on my knowledge of football.
   - All this and and more details can be found in the script 'scraping.ipynb'

2. **Principal Component Analysis PCA**
   - Some statistics are less relevant than others. An interesting tool to reduce the dimensionality of some variables is PCA. I chose the less relevant statistics and did a PCA on them.
   - More about pca on [1]. 
   - From [fifaratings.com](https://www.fifaratings.com/) I retrieved the ratings for the teams I will use in part three 
   - after PCA the new DataFrame is `df_pca.csv`.
   - All this and and more details can be found in the script 'pca.ipynb'
     
3. **Model : Random Forest**
   - I have created other indices that I will use as predictors in the random forest, taking my cue from [2] and [3] . The most interesting index is 'form', defined in the previous article [2].
     Also in the previous article, it is mentioned that goal difference is a relevant predictor.
   - All statistics of a given match entering in random forest are known before each match. So I used for example the average of the expected goals of the previous 3 matches for each team for each match. 
   - After adjusting the parameters separately, I used the best ones to train the algorithm to an accuracy of 68%.
   - More about Random Forest on [4] and [5].
   - The roc curve allows me to find the best threshold [6].
   - Finally, a simple analysis of the most significant parameters
   - All this and and more details can be found in the script'model.ipynb' 


## How to Run
## Project Setup

To follow this project, please ensure you have the following installed locally:

  - [JupyterLab](https://jupyter.org/)
  - [Python 3.8+](https://www.python.org/downloads/)
  - Python packages:
  - [pandas](https://pandas.pydata.org/)
  - [requests](https://docs.python-requests.org/)
  - [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/)
  - [scikit-learn](https://scikit-learn.org/stable/)
  - [matplotlib](https://matplotlib.org/)
  - [seaborn](https://seaborn.pydata.org/)


## Bibliography

1. Holland, Steven M. "Principal components analysis (PCA)." Department of Geology, University of Georgia, Athens, GA 30602 (2008): 2501.

2. Baboota, Rahul, and Harleen Kaur. "Predictive analysis and modelling football results using machine learning approach for English Premier League." International Journal of Forecasting 35.2 (2019): 741-755.

3. Rodrigues, Fátima, and Ângelo Pinto. "Prediction of football match results with Machine Learning." Procedia Computer Science 204 (2022): 463-470.

4. Chen, Xi, and Hemant Ishwaran. "Random forests for genomic data analysis." Genomics 99.6 (2012): 323-329.

5. Cutler, Adele, D. Richard Cutler, and John R. Stevens. "Random forests." Ensemble machine learning: Methods and applications (2012): 157-175.

6. Hoo, Zhe Hui, Jane Candlish, and Dawn Teare. "What is an ROC curve?." Emergency medicine journal (2017).

