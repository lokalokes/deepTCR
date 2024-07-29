# Baseline Model

We had several attempts to get a baseline model working to our satisfaction.

## Baseline Model - Version 1

In our major first attempt, we decided to use only **amino_acids_length_15**  as this [dataset](https://github.com/lokalokes/deepTCR/blob/main/1_DatasetCharacteristics/Testing_length-15.csv) would have all possible positions filled, as shown in the given [screenshot](https://github.com/lokalokes/deepTCR/blob/main/1_DatasetCharacteristics/Screenshot%202024-06-17%20at%2018.43.20.png).

The `deepTCR_baseline_model` involves converting (mapping) letters into numbers based on a predefined [dictionary](https://github.com/lokalokes/deepTCR/blob/main/1_DatasetCharacteristics/dictionary). We started with a simple model.

```python
# Define Parameters
vocab_size = 27  # Assuming 26 letters plus a special character (e.g., space or padding)
embedding_dim = 10  
rnn_units = 64  
batch_size = 1  # Use batch size 1 for prediction later
sequence_length = 15  # Assuming a fixed sequence length of 15


# Build the model
model = Sequential([
    Embedding(vocab_size, embedding_dim, input_length=sequence_length),
    LSTM(rnn_units, return_sequences=False),
    Dense(vocab_size, activation='softmax')
])

model.compile(optimizer='adam', loss='sparse_categorical_crossentropy', metrics=['accuracy'])
```
**[baseline_model.ipynb](https://github.com/lokalokes/deepTCR/blob/main/2_BaselineModel/deepTCR_baseline_model.ipynb)**

## Baseline Model - Version 2
In our second attempt we decided to exclude all 'na' to encourage better predictions.  
**[baseline_model_update.ipynb](https://github.com/lokalokes/deepTCR/blob/main/2_BaselineModel/deepTCR_baseline_model_update.ipynb)**

## Baseline Model - Version 3
The third attempt included removing column 1-3 and the last two colums due to the lack of information. With the model, we tried to predict the fifth position. We run the model for 10, 100 and 1000 epochs to check for  **overfitting** and thereby determine if the model is actually learning. Unfortunately, we made our first big mistake not saving our data on a google drive. Hence, pickle data is not included for this particular model, just the Notebooks. 
   
**[baseline_model_17_06.ipynb](https://github.com/lokalokes/deepTCR/blob/main/2_BaselineModel/deepTCR_model_17_06.ipynb)**  
**[baseline_model_17_06_1000_epochs.ipynb](https://github.com/lokalokes/deepTCR/blob/main/2_BaselineModel/deepTCR_model_17_06_1000_epochs.ipynb)**
