# Charity Data Analysis Neural Network 

The aim of this analysis is to predict if the charity data set will be successful to receive funding or not using  neural network binary classifier.

## Overview of the analysis
This project includes jupyter notebook files that build, train, test the charity dataset, using the TensorFlow Keras `Sequential`
model with `Dense` hidden layers, binary classification as an output layer with different parameters such as

- different epoch numbers
- different hidden layer acrtivation layers


## Results
### Data Preprocessing
loading the [https://github.com/isakovanilu/Neural_Network_Charity_Analysis/blob/master/charity_data.csv](charity_data.csv)
- Target variable: `IS_SUCCESSFUL`
- Features: `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, `ASK_AMT`
- drop `EIN`, `NAME`, since they do not add more value
- binning categorical features
- encode categorical variables using
- split the dataset to train and test
- scale the data

### Compiling, Training, and Evaluating the Model
with the scaled data, build the base model defined in
[`https://github.com/isakovanilu/Neural_Network_Charity_Analysis/blob/master/AlphabetSoupCharity.ipynb`](AlphabetSoupCharity.ipynb)
with the following parameters:
hidden_nodes_layer1 =  80
hidden_nodes_layer2 = 30
with the 'relu' activation

The model summary is shown below:
[https://github.com/isakovanilu/Neural_Network_Charity_Analysis/blob/master/summary_model0.png](summary_model0.png). We then compile and train
the model using the `binary_crossentropy` loss function, `adam` optimizer, and
`accuracy` metric to obtain the training results shown in
[https://github.com/isakovanilu/Neural_Network_Charity_Analysis/blob/master/accuracy0.png](accucary0.png).


The optimized model summary is shown below:
[`https://github.com/isakovanilu/Neural_Network_Charity_Analysis/blob/master/AlphabetSoupCharity_Optimzation.ipynb`](AlphabetSoupCharity_Optimization.ipynb),

hidden_nodes_layer1 =  80
hidden_nodes_layer2 = 30
with the 'tanh' activation

The model summary is shown below:
[https://github.com/isakovanilu/Neural_Network_Charity_Analysis/blob/master/summary_model.png](summary_model.png). We then compile and train
the model using the `binary_crossentropy` loss function, `adam` optimizer, and
`accuracy` metric to obtain the training results shown in
[https://github.com/isakovanilu/Neural_Network_Charity_Analysis/blob/master/accucary.png](accucary.png).


Added more hidden layers

hidden_nodes_layer1 =  100
hidden_nodes_layer2 = 60
hidden_nodes_layer3 = 30
with the 'tanh' activation

The model summary is shown below:
[https://github.com/isakovanilu/Neural_Network_Charity_Analysis/blob/master/summary_model2.png](summary_model2.png). We then compile and train
the model using the `binary_crossentropy` loss function, `adam` optimizer, and
`accuracy` metric to obtain the training results shown in
[https://github.com/isakovanilu/Neural_Network_Charity_Analysis/blob/master/accuracy2.png](accucary2.png).

## Summary
In summary, with the different parameter the accuracy did not reach to 75%.

#### Additional Optimization Methods
The enseble leqrning techniques such as Random forest algorithm can be used to improve the accuracy as an alternative to the ANN. 

