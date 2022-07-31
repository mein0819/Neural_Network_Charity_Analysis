# Neural Network Charity Analysis

## Project Overview

Using loan applicaton data from over 34,000 organizations, a binary classifier is created using neural networks to help predict whether future applicants will be successful if funded by the company Alphabet Soup. The model is developed through the following three steps:
- Preprocessing data for a neural network model
- Compile, train, and evaluate the model
- Optimize the neural network model

## Resources

- Data Sources: charity_data.csv
- Python 3.7.6, Pandas 1.3.4, Jupyter Notebook 6.4.5, TensorFlow 2.9.1

## Results

### Data Preprocessing

- The target variable for the model is the IS_SUCCESSFUL column
- Feature variables were the columns: NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
- Columns NAME, APPLICATION_TYPE, CLASSIFICATION, and ASK_AMT were each binned to group outlier or rare categorical values
- Keeping the NAME column for this dataset was a choice made to test whether the number of times an organization applied for funding had an affect on the outcome

![namebinning](https://github.com/mein0819/Neural_Network_Charity_Analysis/blob/main/readMeImages/nameBinning.png)

- Binning the ASK_AMT column was done to group the wide range of values in the column and clean up outliers to help optimize the dataset

![askamntbinning](https://github.com/mein0819/Neural_Network_Charity_Analysis/blob/main/readMeImages/askAmntBinning.png)

- One variable was dropped from the dataset, EIN

### Compiling, Training, and Evaluating the Model

- The training model was put together using an input and two hidden layers. 80 neurons are used in the input and 30 in the second layer. The the activation functions for the input and second layer were relu, and the sigmoid function was used for output
- Using this revised dataset I was able to reach the target model performance with the same model setup as was used in Deliverable 2. 

![modaccuracy1](https://github.com/mein0819/Neural_Network_Charity_Analysis/blob/main/readMeImages/modAccuracy1.png)

- Having reached the target in the first attempt, I tested the model to see if it could be improved even more. I added a hidden layer with 10 neurons and increased the epochs from 100 to 500. 
