# Data Preparation and Characteristics

## General Approach
 
To obtain data from the **[IMGT database](https://www.imgt.org/)** in a usable format for our purposes, we followed these data manipulation steps:

1. **Install all necessary libraries**

2. **Get the data**
   - fromJson 
   - Filter the data for:
     - **[TRBJ](https://www.imgt.org/IMGTrepertoire/index.php?section=LocusGenes&repertoire=genetable&species=human&group=TRBJ)**
     - **[TRBV](https://www.imgt.org/IMGTrepertoire/index.php?section=LocusGenes&repertoire=genetable&species=human&group=TRBV)**

3. **Manipulate the data (general overview)**  

   3.1 **Encoding the data**
   - Encode AAs in V gene germline sequences  
   - Encode AAs in J gene germline sequences (consider CDR3 length for J genes)  

   3.2 **Rearrange**
   - Get all IMGT positions  
   - Custom function to align CDR3 AA sequences to IMGT  
   - Get a list of patients  

   3.3 **Pivot the data (Column of CDR3s starts with C and ends with F)**
   - Pivot IMGT data  
   - Add IMGT position data to tdata_qc  
   - Exclude the germ line AA  
   - Density of pos_length coverage  
   - Transform each amino acid frequency into a standard normal distribution (INT-transform)  

   3.4 **Transform data into a matrix**
   - Output file: `cdr3.tsv`  

   3.5 **Prepare CDR3 matrix for 34 patients**
   - Output file: **[pivoted_cdr3_subset_34_patients.tsv](https://github.com/lokalokes/deepTCR/blob/main/1_DatasetCharacteristics/pivoted_cdr3_subset_34_patients.tsv)**  

An additional **[heatmap](https://github.com/lokalokes/deepTCR/blob/main/1_DatasetCharacteristics/heatmap_freq.ipynb)** provided an overview what to expect as output data for our model.
<br>

**_Please note_:  
All additional files are relevant in one or another way to the project and are therefore kept for the sake of completeness !!**  
<br>
**[Notebook](https://github.com/lokalokes/deepTCR/blob/main/1_DatasetCharacteristics/cdr3_patient_data.ipynb)**  


