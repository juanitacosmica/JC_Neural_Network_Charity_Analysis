# JC_Neural_Network_Charity_Analysis
Module 19: Neural Networks and Deep Learning Models

# Overview of the analysis:

This project uses machine learning and neural networks, the features in the provided dataset to help creating a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, we have available a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

- D1: Preprocessing Data for a Neural Network Model
- D2: Compile, Train, and Evaluate the Model
- D3: Optimize the Model

# Resources:
 
  **Data source** The csv file is in the Resources Folder as "charity_data.cvs"

  **Software** Jupyter Notebook, Python, Scikit-learn, Pandas, TensorFlow

# Results:

## 1. Data Preprocessing

- What variable(s) are considered the target(s) for your model?

The “IS_SUCCESSFULL” column, the target variables are the dependent variables used to train the Machine Learning Model.

- What variable(s) are considered to be the features for your model?

Also known as the independent variables, considered Features of the Model. They include: all columns, except the target variable and the ones dropped EIN and NAME.

- What variable(s) are neither targets nor features, and should be removed from the input data?

The ones that do not add accuracy to the model, are the ones that should be removed and are not targets or features either as they are not meaningful for the model.
An example of this are the variables with all Unique values, also, we must ensure the outliers and noisy data is taken care of; which can be achieved by dropping the outliers or bucketing.

## 2. Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?

At the end of the optimization and after 3 trial iterations, the final Optimized was achieved using 2 layers, 3 layers increased the loss and did not contribute as much to the accuracy. This might have been because the additional layer may add redundant complexity to the dataset that was already contained within the two layers. That being said, this can help us conclude that adding layer does not mean it will be guaranteed the model performance will be improved; depending on the complexity of the data, adding more layers may only increase the opportunity to overfitting the training data.

The activation functions was RELU as it offered the best accuracy for the model.
200 neurons were used the 1st layer and 90 neurons for the 2nd one. 
Recommendation: The first layer should have at least double the amount of input features which in the case was 100 input values or rows.

For this challenge it was used the adam optimizer, that uses a gradient descent approach to make sure that the algorithm will not get stuck on weaker classifying variables and features and to enhance the performance of classification neural network.

And last but not least, the loss function was binary crossentropy, that is specially designed to evaluate a binary classification model.

The model was trained with 500 epochs, increasing from 200 epoch allowed the model to show a slight improvement, however, the increase was small in order to avoid overfitting.

- Were you able to achieve the target model performance?

Yes. After few iterations and changes in the configuration, the target was met. The model accuracy improved to 76.17%, wherewas previous models were below 72% (shown in the Iterations folder for reference).

- What steps did you take to try and increase model performance?

Step 1: Verified input data and then brought NAME columsn back that had been skipped
Step 2: Added a condition on the values lower than 50 in “Other” group, which helped reducing the number of unique categorical values by binning the values
Step 3: Used bins for the ASK_AMT values
Step 4: Tried adding a 3rd layer with 40 neurons; however, the accuracy did not improve a lot but the loss did increase. 2 layers were definitely better option.
Step 5: Increased neurons for each layer (200 for 1st and 90 for 2nd)
Step 6: Increased Epochs to 500

![What made a huge difference](/Resources/1D2.PNG)

# Summary:

The model loss and accuracy score reflects how well the model performs with the dataset and its configuration and features. 
The loss score is equal to 0.72, meaning the probability model to fail is 72% and the accuracy score is 0.7617, meaning that the probability model to be accurate is 76.17%.

![Final Result after Optimized](/Resources/conclusion.PNG)

- Recommendation for further analysis

Consider adding more input values (if there are available in the original dataset, for example) and having more data, this last point may be sometimes necessary eventhough can be unrealistic depending on the projects.

People call me JC, the short for [Juanita C. Nunez](https://www.linkedin.com/in/juanitacamargonunez/). Contact me for any questions! I love networking, so here you go  my [LinkedIn] (https://www.linkedin.com/in/juanitacamargonunez/) :)


