### Movies and TV review Dataset from Amazon ##

The Data set cannot be uploaded on Github as it is 5.18GB. 
It can be downloaded here: http://jmcauley.ucsd.edu/data/amazon/

### Rundown
File order to run project

- Start with “eda.ipynb” file to get an understanding of the data
- Next open “clean.ipynb” file to clean data for machine learning. At this step files are split in to three folders called clean_train, clean_val, and clean_test. Inside each folder is a csv, the name is “port-xxxx”. Numbers and letters after the port may change based on the environment the code is being implemented in.  The right file path is already in the notebooks but the name of the csv file maybe different. 
- Next open “Machine_learning.ipynb” file to create and train the model
- Next open the “Validation.ipynb” file to test model on new data
- Finally open the “Test.ipynb” file to see the results of the single review


## Project Information

### 1. EDA

For the exploratory data analysis, we explored the count of the overall column and the count of the verified column, categorize the reviews, and found the most frequent words in the dataset. We found that for the overall column there are more fours and fives than ones and twos. When examining the verified column, we saw that there is about 3 times as many true observations as false observations. When splitting the data into short and long reviews we saw that there are more short reviews than long reviews. The most common word in the dataset is movie. 

![Screen Shot 2020-02-22 at 1 30 47 PM](https://user-images.githubusercontent.com/35823055/75097333-92c3dc00-5577-11ea-8253-ab42d8cdc6d5.png)

### 2. Data Processing

In the data preprocessing step, we cleaned the text data. Punctuations, numbers and special characters were removed. Also, all words were lowercased. Next the words were tokenized and stop words were removed. The words were then stemmed using lemmatization. Next words that were not longer than 4 characters were removed. The last step was to split the data into train, validation, and test sets.

### 3. Machine Learning

In the machine learning step, we created a pipeline that used a count vectorizer and the function IDF to transform the data. Then we trained a basic logistic regression model to predict if the review was verified or not. The threshold was change to better fit the imbalanced dataset. Lastly the training data was tested on the model to see how the model was performing.

### 4. Validation

In the validation step the trained model and pipeline was tested on data that the model has not seen before. The metric used to examine the results were ROC, accuracy, and f1 score. Also, recall and precision for one and zero was examined.

![Screen Shot 2020-02-22 at 1 31 49 PM](https://user-images.githubusercontent.com/35823055/75097343-b6872200-5577-11ea-982e-c8f3db888bb3.png)

### 5. Testing 

In the final step we create an application that exports if the review is verified or not.
![Screen Shot 2020-02-22 at 1 32 28 PM](https://user-images.githubusercontent.com/35823055/75097350-cd2d7900-5577-11ea-8003-3256915eacec.png)


