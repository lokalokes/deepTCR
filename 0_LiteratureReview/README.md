# Literature Review

Approaches or solutions that have been tried before on similar projects.

**Summary of Each Work**:

- **Source 1**:  **<ins>Linguistically inspired roadmap for building biologically reliable protein language models</ins>**

  - **[Link](https://doi.org/10.1038/s42256-023-00637-1)**
  - **Objectives**:  
    Deep neural-network-based language models (LMs) or sequence models (e.g., BERT, RoBERTa and GTP) are applied to large-scale protein sequence data to predict protein function. Guidance drawn from linguistics, a field specialized in analytical rule extraction from natural language data, can aid with building more interpretable protein LMs that are more likely to learn relevant domain-specific rules. Differences between protein sequence data and linguistic sequence data require the integration of more domain-specific knowledge in protein LMs compared with natural language LMs.
  - **Methods**:  
    The authors provide a linguistics-based roadmap for protein LM pipeline choices with regard to training data, tokenization, token embedding, sequence embedding and model interpretation.
  - **Outcomes**:  
    Incooperating linguistic ideas into protein LMs enables the development of next-geneation interpretable machine learning models with the potential of uncovering the biological mechanisms underlying sequence-function relationships.
  - **Relation to the Project**:  
    The paper describes three types of methology (architecture analysis, linguistic experimentation and grammatical interference) with their advantages as well as their disadvantages. In addition, the authors point out that the final goal is systematically investigating aspects of LMs that may make a difference for successful sequence-function rule learning before scaling to larger models.

- **Source 2**: **<ins>DeepTCR is a deep learning framework for revealing sequence concepts within T-cell repertoires</ins>**

  - **[Link](https://doi.org/10.1038/s41467-021-21879-w)**
  - **Objective**:  
    The authors present DeepTCR (T-cell receptor), a suite of unsupervised and supervised deep learning methods able to model highly complex TCR sequencing data by learning a joint representation of a TCR by its CDR3 sequences and V/D/J gene usage. They demonstrate the utility of deep learning to provide an improved featurization of the TCR across multiple and murine datasets.
  - **Methods**:  
    The processing flow is as followed: (1) Data curation (2) Data transformations (3) TCR featurization block (4) Training VAE (5) Quantifying TCR distance (6) Clustering antigen-specific TCR sequences (7) Training K-nearest neighboor (KNN) algoritm on TCR sequences (8) Training receptor classifier (9) Training repertoire classifier (10) Motif identification (11) Statistical tests and machine learning models
  - **Outcomes**:  
    A deep learning approach through the use of convolutional neural networks (CNNs) has been used to extract important features from sequencing data for both descriptive and predictive purposes. The authors present DeepTCR, a platform of both unsupervised and supervised deep learning that is able to be applied at the level of the T cell receptor sequences as well as at the level of the whole T cell repertoires.
  - **Relation to the Project**:    
    The paper describes in detail *Unsupervised TCR sequence representation*, *Supervised TCR sequence classification*, *Supervised TCR sequence regression*, *Supervised TCR repertoire classification* as well as *Characterization of TCR repertoire to HIV-specific epitopes* as an example. 

- **Source 3**: **<ins>Deep learning for computional biology</ins>**

  - **[Link](https://doi.org/10.15252/msb.20156651)**
  - **Objective**:     
    The paper provides an overview of different approaches of machine learning in genomics and imaging highlighting possible pitfalls and limitations to guide computional bologists when and how to make the most use of different tools in deep learning for computional biology.
  - **Methods**:  
    The authors present different tools for deep learning for computional biology. Of interest for us is amongst others *Data normalization for and pre-processing for deep neural networks* (Figure 5) - *Partiioning data into training, validation and test sets* to start with.
  - **Outcomes**:  
    The authors come to the conclusion that deep learning methods are a powerful complement to classical machine learning tool and other analysis strategies and expecting further improvements in the near future.
  - **Relation to the Project**:  
    The first half of the paper might be of special interest as it describes in detail *Deep learning for regulatory genomics* providing a road map for building a model using neural networks (Figure 2).

- **Source 4**: **<ins>Deep convolutional neural networks for pan-specific peptide-MHC class I binding prediction</ins>**
  
  - **[Link](https://doi.org/10.1186/s12859-017-1997-x)**
  - **Objective**:    
    Deep convolutional neural network (DCNN) is used to extract low-level features from the ILA (image-like array) and combines them into high-level features (motifs) through multiple convolutional and pooling layers. The DCNN learns these high-features to be used for classifying the input ILA into binder or non-binder through fully connected layers.
  - **Methods**:  
    The paper outlines the full DCNN architecture: Three convolution blocks with two convolution layers and a max pooling layer are concatenated, and three classification layers are then connected to the ends of the network. The dropout was next applied to each convolution block as a regularization. ReLU was used for the nonlinear transformation of the output value of each convolution layer. After training the data an independent evaluation of the DCNN was enforced for validation.
  - **Outcomes**:  
    The authors developed a novel method for peptide-HLA-I binding predictions using DCNN trained on ILA data that encode peptide binding data and demonstrated the reliable performance of the DCNN in nonapeptide binding predictions through the independent evaluation on the latest IEDB benchmark datasets. In addition, they build a web server ConvMHC for peptide-MHC class I binding predictions using DCNN (Figure 5)
  - **Relation to the Project**:  
    *The approach can be applied to characterize locally-clustered patterns in molecular interactions, such as protein/DNA, protein/RNA, and drug/protein interactions.*  
    The full DCNN architecture needs to be investigated ;-)
