# Model Definition

After evaluating our baseline model and extensive discussions, we decided to improve our model with **LSTM** predicting the fifth position (removing column 1-3, -2 + some middle positions ZEROs removed).  

The overall objective of this model is to process sequential data (sequence of amino acids in the random part of a receptor) and predict the next letter (amino acid) in the sequence. This type of model is commonly used in natural language processing tasks such as language modeling, text generation, and machine translation. The multiple LSTM layers allow the model to capture complex dependencies and patterns in the input sequences, while the dense layers help in refining and processing the features extracted by the LSTM layers.



```python
# Define parameters
vocab_size = 21  # 20 amino acids
embedding_dim = 8
rnn_units = 32
sequence_length = 4
batch_size = 1  # Use batch size  for prediction later

# Build the model
model = Sequential([
    Embedding(vocab_size, embedding_dim, input_length=sequence_length),
    LSTM(rnn_units*2, return_sequences=True),
    Dense(128, activation = "relu"),
    Reshape((sequence_length, 128)),
    LSTM(rnn_units, return_sequences=True),
    Dense(64, activation = "relu"),
    Reshape((sequence_length, 64)),
    LSTM(rnn_units),
    Dense(vocab_size, activation='softmax')

])

model.compile(optimizer=Adam(learning_rate=0.001), loss='sparse_categorical_crossentropy', metrics=['accuracy'])
```

This time we saved the pickle data for both 100 and 1000 epochs ;-)
   
**[deepTCR_model2_100.ipynb](https://github.com/lokalokes/deepTCR/blob/main/3_Model/deepTCR_model2_100.ipynb)**  
**[deepTCR_model2_1000.ipynb](https://github.com/lokalokes/deepTCR/blob/main/3_Model/deepTCR_model2_1000.ipynb)** 

# Model Evaluation

## Baseline Model
	(predicting the fifth position (removing column 1-3, -2)
	-> 1000 epochs: High Training Accurancy 67 % + Learning + Overfitting
	-> Predicted mainly ZEROs 

## Model with LSTM
	(predicting the fifth position (removing column 1-3, -2 + some middle positions ZEROs removed)
	First version  
		30 epochs
		100 epochs
		1000 epochs with increased batch sizes
  
```python
# Train the model
history =  model.fit(training_set_X, training_set_y, epochs=1000, batch_size = 32, validation_split =0.2)
```

  -> High Training Accurancy 65 % + **_not Overfitting_**

## Conclusion
We could not archive **_Overfitting_**. Therefore, we conclude that data is indeed **_RANDOM_**.

## Outlook

However, as scientists we should consider additional strategies to increase model accuracy:

#### Enhance the Model Architecture:

- **Add More Layers:** Increase the depth of the model by adding additional LSTM or dense layers.
- **Increase Units:** Increase the number of units in the LSTM layers.
- **Bidirectional LSTM:** Utilize Bidirectional LSTMs to capture patterns from both directions.

#### Tune Hyperparameters:

- **Learning Rate:** Adjust the learning rate of our optimizer.
- **Batch Size:** Experiment with different batch sizes.
- **Dropout:** Incorporate dropout layers to prevent overfitting.

#### Improve Data Quality:

- **_More Data:_** _Increase the amount of training data and the number of patients_ !!
- **Data Augmentation:** Apply techniques to generate more training examples.
- **Data Cleaning:** Ensure the data is clean and properly preprocessed.

#### Regularization Techniques:

- **Dropout:** Add dropout layers to reduce overfitting.
- **L2 Regularization:** Apply L2 regularization to the dense layers.

#### Advanced Techniques:

- **Transfer Learning:** Utilize pre-trained embeddings such as GloVe or Word2Vec.
- **Hyperparameter Tuning:** Implement techniques like grid search or random search to find the optimal hyperparameters.
