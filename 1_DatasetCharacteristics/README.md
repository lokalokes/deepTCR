# Data Preparation and Characteristics

## General approach
 
To obtain data from the **[IMGT database](https://www.imgt.org/)** in a usable format for our purposes, we followed these data manipulation steps:

#### 1. Install all the necessary librabries
	
#### 2. Get the data
	- fromJson 
	- filter the data 
		- **[TRBJ](https://www.imgt.org/IMGTrepertoire/index.php?section=LocusGenes&repertoire=genetable&species=human&group=TRBJ)** and 
		- **[TRBV](https://www.imgt.org/IMGTrepertoire/index.php?section=LocusGenes&repertoire=genetable&species=human&group=TRBV)**
	
#### 3. Manipulate the data (general overview)
   
##### 3.1 Encoding the data
	- AAs encoded in V gene germline sequences
	- AAs encoded in J gene germline sequences (we need to consider CDR3 length for J genes)
##### 3.2 Rearrange
	- Get all IMGT positions
	- Custom function to align CDR3 AA seq to IMGT
	- Get a list of patients
##### 3.3 Pivot the data (Column of CDR3s starts with C and ends with F) 
	- Pivot imgt
	- Add imgt position data to tdata_qc
	- Excluding the germ line AA
	- Density of pos_length coverage
	- Transform each armino acid frequency into a standard normal distribution (INT-transform)
##### 3.4 Transform pall into a matrix
	-> Output file 'cdr3.tsv'
##### 3.5 Preparing cdr3 matrix for 34 patients of CDR3s
	-> Output file **[pivoted_cdr3_subset_34_patients.tsv](https://github.com/lokalokes/deepTCR/blob/main/1_DatasetCharacteristics/pivoted_cdr3_subset_34_patients.tsv)**

**[Notebook](https://github.com/lokalokes/deepTCR/blob/main/1_DatasetCharacteristics/cdr3_patient_data.ipynb)**

