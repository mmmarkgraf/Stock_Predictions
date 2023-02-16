# Stock_Predictions
Using machine learning, I successfully created machine learning models that were able to predict the movement/direction of stock
prices under normal market conditions. However, the models under the current market economy that is being affected by the 
pandemic will not be able to predict with sufficient success. Until the market improves, this project has been stopped due to 
there being no relevant historical financial data to aid in the training of the models.

This project uses Random Forest, AdaBoost, and Gradient Boosting--the results suggest that Random Forest is the best option out 
of the three machine learning models.

(Excuse the low-level coding as this is my first project and it became larger than I had expected. Modular programming was also 
not implemented due to free API keys and web parsing restrictions, which made it impossible to run the first three scripts to
cover all stocks.)

If wanting to only examine specific stocks, simply examine the format of the first few CSV files created and beginning with the 
filename "merged_NYSE_AMEX". Then create your own custom CSV file (or create a new Pandas DataFrame) using the same format and 
replace the scripting code in all scripts to only load your custom file.

The PDF PowerPoint presentation outlines the general steps and current outcomes of the project. 
    ("Stock Predictions - PDF Predictions")
There is another PDF that goes more in-depth about the ideas and reasons for the project, as well as some data analysis.
    ("Stock Predictions - Thesis")

Do note that this project still requires a lot of work and many improvements can be made. However, due to limited time, I am 
currently unable to implement any further changes.

Storage requirement of this project requires more than 15+ GB of free space.


(This project was originally completed as a student capstone project for SpringBoard, which is reflected in the project thesis.)


______________________________________________________________________________________________________________________


Version 0.01


    The purpose of this GitHub project is to predict stock prices using ensemble machine learning techniques
    (Random Forest, AdaBoost, Gradient Boosting).
    
    Listed below are the steps and orders the iPython Notebooks should be run in.
    Before starting, two API keys should be obtained (they are free):
        - Alpha Vantage API
        - New York Times API
    
    The lists of stock names were obtained in Jan. 2020 and does not include any new companies that have recently IPO-ed.
        
    Estimated time to complete running all the scripts as they are currently written:
        - 15-25 Days (limited by the New York Times API, Google web parsing, and computing power)
        
    The script that will take the longest to run (continuously) is the Price_Predict_GITHUB script.
    - Changing the number of trees to train for the models will dramatically decrease the processing time.
    - It is recommended to create multiple copies of this script and looping through different sets of stocks to 
      maximize CPU usage
        - Python/iPython/Juypter/Sklearn will not maximize CPU usage and will not utilize GPU when computing.
    
    Publishing (or the likes) on and of these scripts is not allowed.


Run the scripts in this order:

1st:
A - Alpha_Vantage_API_Price_Daily_GITHUB
B - Times_API_Historical_Data_GITHUB
B - Google_News_Web_Parsing_GITHUB
C - Earnings_Extraction_Yahoo_Finance_GITHUB

2rd:
A - Base_Score_GITHUB
B - Evalutating_Words_Looper_GITHUB
D - Patterns_Finder_GITHUB

3rd:
C - Earnings_Combine_GITHUB
D - Average_of_Dates_Before_MA30-60_Intercept_Pattern_GITHUB

4th:
C - Earnings_Score_GITHUB
D - Stats_Linear_Regression_Fit_Moving_Average_Pattern_GITHUB

5th:
D - Patterns_Score_GITHUB

6TH:
A, B, C, D = E - Final_Table_Creater_GITHUB

7TH:
E = F - Price_Predict_GITHUB

8TH:
F - Prediction_Analysis_Visualization_GITHUB
E, F = G - Prediction_Analysis_Looper_GITHUB
