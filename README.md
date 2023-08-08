# **Deep-Learning-Challenge**
## Module 21

## **Overview:** 
In this project, I explored the process of building a model to predict the potential success of future applicants. The answers below describe the mentality and tactics used to achieve this goal. 

## **Results:** 
### Version 1 (Starter Code)
Total Params = 5,981
Loss = 0.5565
Accuracy = 0.7256
### Version 2 (Optimized)
Total Params = 1,241
Loss = 0.5528
Accuracy = 0.7276


## **Data Pre-Processing:**
### 1A - What variable(s) are the target(s) for your model?
The task was to create a tool to better identify potential ventures with higher chances of success. Considering that, the metric “ IS_SUCCESSFUL” was the primary variable being trained on. 
### 1B -What variable(s) are the feature(s) for your model? 
In my efforts, I used the binned data from the columns “APPLICATION_TYPE”, “CLASSIFICATION”, “ASK_AMT”, and “INCOME_AMT” for the training model. Further research would be needed to determine what the different grades of APPLICATION_TYPE, as including other columns may be needed unless these are determining factors to said grade. 
### 1C - What variables(s) should be removed from the input data due to lack of relevance?
Some of the first information removed from training was the inquiries’ “EIN” and “NAME”, which are unrelated to the success of the campaign. Five of the remaining 10 columns were ignored for the time being, but further investigation of these columns may prove prudent (unless deemed redundant through the APPLICATION_TYPE grading system). 

## **Building+Training+Evaluation the Model:**
### 2A - How many neurons/Layers/activation functions did I use and why
Version 1: 2 layers with 80/30 node spread and relu activation type to best match the sample code / set a baseline. 
Version 2: This also consisted of 2 layers but with the nodes reduced to 20/10 due to the limited amount of variables being trained on. Layer 2’s activation was changed to “LeakyReLU” as it showed marginal improvement through some testing. 
### 2B - Were you able to achieve the target performance of 75% accuracy? 
Version 1: This build proved unsuccessful in achieving the target performance. Code performed similarly to the sample code, with both only reaching 72.5% model accuracy.
Version 2: The second attempt also proved unsuccessful in achieving the target performance. This second model had marginal improvements over the original build showing a +0.2% Accuracy and -0.37% Loss. Further R/D is advised to better reach the target performance 
### 2C - What steps did you take in your attempts to increase model performance?”
Version 1: The original model’s primary purpose was to best match the sample code provided. This was used as a proof of concept, and a building point for future models. Increasing this model’s performance wasn’t my primary focus during development. 
Version 2: During the second attempt, I tried lowering the Node Count (due to the smaller training size), adding a 3rd layer (and later removed as it wasn’t beneficial), and expanding the training size used (hoping that the model would have more to train on). These showed marginal improvements, but none of the mentioned attempts resulted in a model reaching the target performance. 

## **Summary:**
In the efforts of trying to create a Machine Learning model capturing the success rates of campaigns remains a challenge for me. I believe the small size of the dataset with limited features is the primary reason the model failed to reach/exceed a rating of 75% accuracy. It’s possible that expanding the dataset using some of the ignored columns or exchanging the columns previously used may show higher results. Further experimentation would be needed to determine if a higher accuracy rating is possible given the available data. 
