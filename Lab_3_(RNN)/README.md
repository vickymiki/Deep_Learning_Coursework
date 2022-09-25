## Objectives:

- Use recurrent neural networks for text classification
- Use recurrent neural networks for timer series regression


## Q1) Recurrent Neural Network for Text Classification

### Q1.1) RNN Model 
Define a recurrent neural netowrk model for this classification task. You model should contain the following:
- `An embedding layer` that is initialized with pre-trained word vectors and can fine-tune the word vectors (as we noticed from HW 3, this configuration worked the best)
- One or more `RNN layers (LSTM or GRU)`
   
### Q1.2) RNN + CNN Model

Define a model with RNN and CNN layers working together.

You model should contain these layers in the order as follows:
1. `An embedding layer` that is initialized with pre-trained word vectors and can fine-tune the word vectors (as we noticed from HW 3, this configuration worked the best)
2. One or more `RNN layers (LSTM or GRU)`: If your sequence length is L, and the RNN hidden units is M, the RNN layers will output a sequence of shape `L x M` or `L x 2M` (for bidirectional). In other words, each element in the sequence has been transformed into a vector of size `M` (or `2M`).
3. `CNN layers` (as you defined in HW3): The CNN layers continue to process the sequence produced by the RNN. For CNN layers, feel free to use your code in HW3 or the reference solution 
   
Train this model as Q1.1. You are expected to receive `an accuracy around 91% on the test dataset`.

### Q2.1) Preprocessing

Write a function `transform_data(data, feature_cols, target_col, cut_off_index, timestep=8)` to transform the dataset to a format that can be used by RNN. 
### Q2.2) Establish a naive baseline

Create a function `evaluate_naive_method` to estalish a baseline.

### Q2.3) Create train, evaluation, and test dataset

### Q2.4) Define RNN model

Create a neural network model as follows:
    - The input to the model is the the training samples you created in Q2.1. 
    - Add LSTM or GRU layers into the model
    - Add other appropriate layers or mechanisms, e.g. Dropout, regularizers.
    - The output predicts the transformed `cnt` value of the next hour 
    - Carefully choose your hyperparameters, e.g. the number of hidden units in the LSTM/GRU layer, epochs, batch size etc.
   
   
### Q2.5) Define a train function


