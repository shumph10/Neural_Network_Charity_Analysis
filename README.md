# Neural_Network_Charity_Analysis
Analysis of organization funding criteria for a non-profit group that sources organizations with a focus on interpersonal, environmental, and worldwide wellbeing.


-----------------------------------

##**Resources**
Data Sources: [charity_data.csv](https://github.com/shumph10/Neural_Network_Charity_Analysis/blob/main/charity_data.csv)
Software: Python 3.9.7, Google CoLab

-----------------------------------

##**Overview**

Analysis of organization funding criteria for a non-profit group that sources organizations with a focus on interpersonal, environmental, and worldwide wellbeing. Factors influencing application approval or denial in the past were put through keras machine learning to develop a trained algorithm which could review future applicants information and predict those likely to get approved and use funds well. This ensures the protection of the non-profits funds on the basis that approved applicants will not misuse and thus waste funds.

The data given was cleaned to remove that which was not useful to the model, such as organization name and categories were bucketed to ensure outliers would not influence the overall model. These categories were then incoded to work with the deep learning model and original categorical columns were removed. The data was scaled to ensure larger base values were weighted appropiately. The Tensor Flow Keras module was used to implement a neural network which will use Relu activation functions to evaluate information and the output layer uses the sigmoid activation function to provide a probability of new organizations being approved or denied. The model was evaluated on its loss and accuracy and saved as an H5 file.


-----------------------------------


##**Data Preprocessing**

- The target variable for the model was the application approval/denial. Once encoded the yes/no for this field was redudunt so only the application approved column was kept. This was assigned as the y or dependent variable for the training/test.
- The variables that were considered to be features of the model were the application type, classification of the organization, organization type, income amount, and special considerations if any. These values were bucketed if there were more than 10 values to ensure proper weighting of the model and remove outliers since it is not likely they will be of major influence a neural network model. 
- The variables that are neither targets nor features are those than cannot be taken in by neural network machine learning models. These would be the names of organizations and their corresponding EIN numbers. 


-----------------------------------

##**Compiling, Training, and Evaluating the Model**
- For the model, I chose to have 2 hidden layers as it is therorized that almost any model can be succesfully completed with three layers so two should be sufficent for a data set of this size while still attempting the most accurate results. For the input layer, I decided to use 80 nodes in the first hidden layer since the number of input features(or number of features in the encoded, cleaned dataset) was 42, so I doubled that number. For the second hidden layer, I decreased that amount to improve run time to about under half, going with 30. The output layer had one node so the output would be binary. 
- Model accuracy was 46.6% and loss was 69.9% so I would not say target model performance was met and further evaluation of the input data or parameters used would need to be done to improve it. I would determine the minimum model accuracy to be around 90% since the non-profit is using it as a determine factor for major funding expenses. The loss should be well below 10% for the same reason. Since the non-profit has awarded millions of dollars since its funding high accuracy is needed as organizations could potentially be receiving high amounts of funding. 
- In order to increase performance I would create a function that uses kerastuner to decide the number of neurons and activation function for each layer. This would provide the best possible hyperparameters for a high accuracy model.


-----------------------------------

##**Summary**

Overall the model did not meet personal requirements of accuracy or loss metrics for use in the prediction of approval of organizations for funding by this non-profit. Since the non-profit focuses on world improvements on both the personal and environment, their money is carefully placed into the hands of those who share similar ideals and goals. Therefore, the risk of funding frauduelent organizations on the basis of a low performance model is not worth the risk to the foundation. Additional measures and data could be implemented to improve the results of the model, allowing use in the future. These include adjustment of neural nodes and layer numbers. 

-----------------------------------

##**Contact Me**

Email: sarahhumphrey2016@outlook.com </br>
[LinkedIn](https://www.linkedin.com/in/sarah-humphrey-data-analyst/)





