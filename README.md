# Neural_Network_Charity_Analysis

##**Overview**

Analysis of organization funding criteria for a non-profit group that sources organizations with a focus on interpersonal, environmental, and worldwide wellbeing. Factors influencing application approval or denial in the past were put through keras machine learning to develop a trained algorithm which could review future applicants information and predict those likely to get approved and use funds well. This ensures the protection of the non-profits funds on the basis that approved applicants will not misuse and thus waste funds.

The data given was cleaned to remove that which was not useful to the model, such as organization name and categories were bucketed to ensure outliers would not influence the overall model. These categories were then incoded to work with the deep learning model and original categorical columns were removed. The data was scaled to ensure larger base values were weighted appropiately. The Tensor Flow Keras module was used to implement a neural network which will use Relu activation functions to evaluate information and the output layer uses the sigmoid activation function to provide a probability of new organizations being approved or denied. The model was evaluated on its loss and accuracy and saved as an H5 file.

##**Data Preprocessing**

- The target variable for the model was the application approval/denial. Once encoded the yes/no for this field was redudunt so only the application approved column was kept. This was assigned as the y or dependent variable for the training/test.
- The variables that were considered to be features of the model were the application type, classification of the organization, organization type, income amount, and special considerations if any. These values were bucketed if there were more than 10 values to ensure proper weighting of the model and remove outliers since it is not likely they will be of major influence a neural network model. 
- The variables that are neither targets nor features are those than cannot be taken in by neural network machine learning models. These would be the names of organizations and their corresponding EIN numbers. 

##**Compiling, Training, and Evaluating the Model**
- For the model, I chose to have 2 hidden layers as it is therorized that almost any model can be succesfully completed with three layers so two should be sufficent for a data set of this size while still attempting the most accurate results. For the input layer, I sho
