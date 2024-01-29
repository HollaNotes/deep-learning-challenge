**<h1>Alphabet Soup Report</h1>**
*<h3>Module 21 Challenge - Deep Learning Challenge</h3>*





**1.	Overview of the analysis:** *Explain the purpose of this analysis.*

- The purpose of this analysis is to attempt to create a tool that would predict applicants with the highest chance of success for the nonprofit organization, Alphabet Soup.

**2.	Results:** *Using bulleted lists and images to support your answers, address the following questions:*

-   **Data Preprocessing**
	- *What variable(s) are the target(s) for your model?*
    	- "IS_SUCCESSFUL"
	- *What variable(s) are the features for your model?*
    	- "APPLICATION_TYPE"
        - "AFFILIATION"
        - "CLASSIFICATION"
        - "USE_CASE"
        - "ORGANIZATION"
        - "STATUS"
        - "INCOME_AMT"
        - "SPECIAL_CONSIDERATIONS"
        - "ASK_AMT"
	- *What variable(s) should be removed from the input data because they are neither targets nor features?*
    	- "EIN"
    	- "NAME"

- **Compiling, Training, and Evaluating the Model**
	- *How many neurons, layers, and activation functions did you select for your neural network model, and why?*
    	- I initially set my model to 2 hidden layers. I set the first layer to 86 neurons with the relu activation function. I set the second layer to 43 neurons with the relu function. I decided to start with 86 neurons because one of the notes in the 21.2 class Readme said, "In general, when building the initial model, we should use 2–3 times as many neurons as there are input features." so I figured doubling the input dimension would be a good place to start. This lead to a model performance of *72.59%* accuracy.
	- *Were you able to achieve the target model performance?* 
    	- No, I was unable to achieve the target model performance of 75%.
	- *What steps did you take in your attempts to increase model performance?*
    	- **Optimization Attempt 1** - In my first optimization attempt, I tried to increase model performance by adding an additional hidden layer. This lead to a model performance of *72.48%* accuracy.
    	- **Optimization Attempt 2** - In my second optimization attempt, I tried to increase model performance by decreasing neurons to my first 2 layers. This lead to a model performance of *72.79%* accuracy. 
    	- **Optimization Attempt 3** - In my second optimization attempt, I tried to increase model performance by increasing the number or epochs. This lead to a model performance of *72.52%* accuracy.
    	- **Optimization with hp.Choice** - I decided to try and find the best optimization parameters for this model by using auto optimization. After getting low results, I wanted to see if there was another way to optimize my model that would yield wildly different results. Unfortunately, this only lead to a model performance of *72.89%* accuracy.


**3.	Summary:** *Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.*
- Overall, the results of the deep learning model were not strong enough to be able to use as a tool to predict applicants with the highest chance of success. Although I was able to play around with the model to see if I could improve upon the accuracy, I was unable to get my model to perform at 75% accuracy. Even when performing an auto-optimization, the highest accuracy I was able to achieve was less than 75%. Using a random forest model could be a better way to solve this classification problem by letting you see which features are important and which ones we could leave off in order to improve performance.


