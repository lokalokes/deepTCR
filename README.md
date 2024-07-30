# Disentangling patterns of T cells
# by Evgeniya Lokes and Janine Berndt  


## [Repository Link](https://github.com/lokalokes/deepTCR)


## Description

### Project Overview:
This deep learning project aims to analyze T cell receptor (TCR) repertoires to better understand immune responses and identify potential patterns of diseases. TCRs are crucial components of the adaptive immune system, with their diversity and specificity playing a vital role in recognizing and responding to pathogens and abnormal cells.

### Objectives:

- Data Preprocessing: Collect and preprocess TCR sequence data from high-throughput sequencing experiments. This includes cleaning, normalizing, and encoding the sequences for input into deep learning models.
- Model Development: Develop deep learning models, such as recurrent neural networks (RNNs) or convolutional neural networks (CNNs), to classify TCR sequences and predict their sequence specificities.
- Feature Extraction: Utilize the models to extract meaningful features from the TCR sequences that correlate with immune responses.
- Patterns Discovery: Identify potential patternns of diseases by analyzing associations and correlations in the TCR repertoire data.

### Key Steps:

- Data Collection: Gather TCR sequence datasets from public repositories.
- Sequence Encoding: Convert TCR sequences into numerical representations suitable for deep learning (e.g., one-hot encoding or embedding layers).
- Model Training: Train deep learning models on labeled datasets to learn the features and patterns associated with different immune responses.
- Model Evaluation: Validate the models using cross-validation techniques and test sets to ensure robustness and accuracy.
- Interpretation: Analyze the model outputs to interpret the biological significance of the findings and validate the results with experimental data.

### Challenges:

- Data Complexity: Handling the high dimensionality and variability of TCR sequences.
- Biological Interpretation: Translating model predictions into meaningful biological insights.
- Limited Labeled Data: Addressing the scarcity of labeled datasets for specific diseases or conditions.

### Impact:
This project has the potential to enhance our understanding of immune responses and improve the diagnosis and treatment of diseases by leveraging the power of deep learning to analyze complex TCR repertoire data.

### Results Summary

- **Best Model:** deepTCR_model2
- **Evaluation and Result:**  
  High Training Accurancy 65 % + could not archive **_Overfitting_** --> Data is **_RANDOM_**!

## Documentation

1. **[Literature Review](0_LiteratureReview/README.md)**
2. **[Dataset Characteristics](1_DatasetCharacteristics/README.md)**
3. **[Baseline Model](2_BaselineModel/README.md)**
4. **[Model Definition and Evaluation](3_Model/README.md)**
5. **[Presentation](4_Presentation/README.md)**

## Cover Image

[Project Cover Image](https://github.com/lokalokes/deepTCR/blob/main/CoverImage/TCR.png)
