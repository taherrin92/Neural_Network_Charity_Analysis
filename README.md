# Neural_Network_Charity_Analysis

Alphabet Soup's business team sent a csv containing the funding of over 34000 businesses. They want to know which of these businesses have been successful. In order to process all of this information, a neural network machine learning model was constructed. First the data was preprocessed to be run in the neural network, then we trained and evaluated the model, and optimized it in an attempt to bring the accuracy of the model above 75%.

## Results

### Data Preprocessing
The target variable considered was the IS_SUCCESSFUL column. All other columns were considered as features except the EIN and NAME columns, which were dropped as they were determined to be neither targets nor features.

### Compiling, Training, and Evaluating

 - Two hidden layers were added into the initial model with the first layer having 8 neurons and the second layer having 5. By narrowing the number of neurons down, data that "passes" the first layer needs to be filtered through fewer neurons, otherwise there is no need for a second layer. 

 - The relu activation function was used in the hidden layers to reduce "unsuccessful" features to zero, and "successful" features passed into the second layer. The output layer used a sigmoid activation function creates a plot for inputs to outputs.

The accuracy of the initial model was 53%, falling short of the target 75%.

### Optimizing the Model

For the attempts to optimize the model, the EIN, NAME, USE_CASE, and STATUS columns were ejected from the model. 

 - The first optimization attempt added an extra layer and increased the number of neurons in the model, and the Accuracy improved to 72.3%

 - The second attempt added a fourth layer and doubled the neurons. The hidden layer activation functions were changed to tanh, and the Accuracy improved to 72.6%
 
 - The third attempt kept the layers and neurons constant, but essentially switched the activation function types used in the initial model. Sigmoid activation functions were used in the hidden layers, and a linear activation function was used for the output. This increased the accuracy to 72.7%

### Summary

Even though the model was not able to reach 75% accuracy, it only fell short by 2.3%. The optimization attempts were only slight improvements over each other, but a huge improvement over the initial model. This could be be fixed by optimizing the number of neurons in each layer as well as removing one or two more features. 
