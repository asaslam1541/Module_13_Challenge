# Module_13_Challenge: Alphabet Soup Neural Network Analysis

This project involves building and analyzing multiple neural network models to predict the success of startups funded by Alphabet Soup. The models are optimized to improve predictive accuracy, and the results of each model are compared for evaluation.

## Data Preprocessing

- **Read Data:** The `applicants_data.csv` file is read into a Pandas DataFrame.
- **Review Data:** The DataFrame is reviewed to identify categorical variables for encoding and to determine features and target variables.
- **Drop Columns:** Irrelevant columns such as "EIN" and "NAME" are dropped from the DataFrame.
- **Encode Categorical Variables:** Categorical variables are encoded using OneHotEncoder and placed in a new DataFrame.
- **Combine Data:** Numerical variables from the original DataFrame are added to the DataFrame containing the encoded variables.
- **Create Features and Target:** Features (X) and the target (y) datasets are created. The "IS_SUCCESSFUL" column defines the target dataset.
- **Split Data:** The features and target datasets are split into training and testing datasets.
- **Scale Data:** StandardScaler from scikit-learn is used to scale the features data.

## Original Neural Network Model

- **Design Model:** A binary classification deep neural network model is designed using TensorFlow's Keras. The number of input features, layers, and neurons on each layer are determined.
- **Compile Model:** The model is compiled using the binary_crossentropy loss function, the Adam optimizer, and the accuracy evaluation metric.
- **Fit Model:** The model is fitted using the training data.
- **Evaluate Model:** The model is evaluated using the test data to calculate loss and accuracy.
- **Save Model:** The model is saved as an HDF5 file named "AlphabetSoup.h5".

## Model Optimization

- **Alternative Models:** Two new deep neural network models are defined, each with different architectures and hyperparameters to improve predictive accuracy.
- **Display Results:** The accuracy scores achieved by each model are displayed and compared.
- **Save Models:** Each model is saved as an HDF5 file for future use.

# Models

## Original Model

- **Number of Hidden Layers:** 2
- **Hidden Layer 1 Nodes:** 15
- **Hidden Layer 2 Nodes:** 20
- **Activation Functions:** ReLU and ELU
- **Epochs:** 100

### Results:

- **Loss:** 0.55196
- **Accuracy:** 72.77%

## Alternative Model 1

- **Number of Hidden Layers:** 3
- **Hidden Layer 1 Nodes:** 10
- **Hidden Layer 2 Nodes:** 12
- **Hidden Layer 3 Nodes:** 16
- **Activation Functions:** ELU
- **Epochs:** 50

### Results:

- **Loss:** 0.55323
- **Accuracy:** 72.91%

## Alternative Model 2

- **Number of Hidden Layers:** 2
- **Hidden Layer Nodes:** 16, 18
- **Activation Functions:** ReLU, Softmax
- **Epochs:** 50

### Results:

- **Loss:** 0.69148
- **Accuracy:** 52.92%

## Conclusion

The original model achieved the highest accuracy at 72.77%, while Alternative Model 1 slightly improved the accuracy to 72.91%. However, Alternative Model 2 performed poorly with an accuracy of 52.92%.

For all models, we had 116 input features and one output. The number of hidden layers, nodes, and activation functions varied among the models to explore different architectures.

