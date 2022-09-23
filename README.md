# Bioinformatics

## OMICs DATA 
the post genomic era has rediated its influnence and brought about advances in the pursuit of information underpinning
other biological entities

Genes --> genomics
proteins --> Proteomics
Sugar --> Glycomics
Lipds --> Lipidomics
Metabolites --> Metabolomics
Molecular Intercations --> interactomics

In the case of drug-design we consider protein-ligand interactions, so we use interactOMICs.

OMICs (provides basic informations of disease) + Precision Medicine +  Bioinfromatics

OMICS data are often large and complex and reliant on Bioinformatics technology to make sense and 
translate such data to actionable insights 

Bioinformatics is a field that applies statistics and information theory to 
make sense of biological data

Bioinformtics lies at the interface of bilogy and computer science 

Common Tasks in Bioinformatics

Search --> search public databases for information on genes/proteins/RNA/pathways (PDB, UNIProt)
Compare --> sequence alighment to discern similarity/differnces amongst varous genes/proteins/RNA
Model --> Build structural model of protein structure (homology modeling for protein) and build predictive models 
using retrospective data
Integrate and curate --> combine heterogeneous data sources, redundancy 

Computational Bilogy --> Applies computational techniques to understand bilogy
Bioinformatics --> Involves the devlopment of algorithms and tools to analyze and solve bilogical data

Bioinformatics Tools --> databases, softwares, webservers that allow users to retrieve , 
analyze and gain insights from bilogical data

## Why do we need computational models for drug design and discovery?? 

* To discern structure-activity relationship (SAR) of chemical library
* In vitro-data are limited, expensive and time consuming, laborious etc.
* Computational models can be quickly built to predict teh pharmacokinetics (ADME/T)  and  bioactivity (inhibition or activation of target protein) of query compounds  
* Models can be used to repurpose existing FDA approved drugs for new therapeutic treatment

## Question that can be answered by Computational Models

* What target proteins could my compounds bind to and modulate?
* Would my compound/s bind unpacifically to other proteins and thus have off-target activity
* What type of compounds can bind and modulate the bioactivity of the target protein of my interest
* Are there similar compounds to my query compound that may potentially exert similar binding behavior
* How does my compound bind to the protein structure of its target 

## Drug Discovery Toolbox

#### Combinatorial Chemistry -- Chemical Libraries -- Chemical Space -- High Throughput Screening -- Property Filters -- Computational Chemistry -- Machine Learning -- QSAR -- Proteo-chemo-metrics -- Molecular Modeling -- Molecular Dynamics -- Molecular Docking

## QSAR 

Data Science (Unstructured Data >> Structured data >> uncover patterns >> gain knowledge >> gain wisdom )

Quantitative structure– activity relationship (QSAR) is ligand-based approach in computational drug design for correlating the molecular features of a chemical library with their respective bioactivity

-Modeling is a mathematical modeling that seeks to discern the relationship between 
the chemical structure and their bioactivity
-The chemical structure is defined by a set of molecular descriptors that can account for local or 
global physicochemical properties
-local features, e.g. the number/presence of specific functional moities (molecular fingerprints)
-Global Features e.g. molecular weight, lipophilicity  
 
Part A - In this solubility prediction project we have reproduced the solubility results of compounds given by Delaney (2004), article is cited in the notebook file

## Procedures for the development of a QSAR model

* Biological Data Collection - The biological activity of a series of compounds is determined experimentally or obtained fro literature

* Descriptor Generation - Physicochemical information encoded within the molecular structure of the compounds is extracted through the use of a wide range of computational chemistry software; for some descriptors geometry optimization prior to descriptor calculation may be required; some descriptors may require molecular structure alignment or superpoistion

* Feature Selection - This is performed to reduce the dimensionality of the feature space as well as remove collinear and redundant descriptors

* Data Pre-processing - This is carried out to ensure the lntegrity and completeness of the data to be analyzed as well as adjusting the data values by scaling them through normalization and standardization methods 

* Training and testing selection - Data set is divided into training and testing set where the former will be used for model development and tested on the latter

* Internal validation - The predictive performance of the model is validated internally using N-fold or leave-one-out cross-validation

* Model development - The training set is used for model development through the use of various learning algorithm 

* Performance evaluation - The predictive performance of the developed model is evaluated through varoius statistical parameters 

* External validation - The predictive perfromance of the developed model in a real-world situation can be elucidated by applying the model on a set of unseen compounds 

Here we also create new QSAR model for Estrogen Receptor Alpha (CHEM206) inhibitory compounds, inspired by the following articles:
https://pubs.rsc.org/en/content/articlelanding/2018/ra/c7ra10979b

The expression of ERa is greatly increased in breast cancer cells and as such represents a promising therapeutic target for combating breast cancer
QSAR has been instrumental in shedding light on the molecular basis of bioactivity of interest by learning from past bioactivity data while also being amenable to extrapolating on the bioactivity of new compounds that are foreign to the trained data set

### PART I

We got bioactivity data for 14662 compounds for CHEMBL206 target protein with multiple bioactivity data, we only extract IC50 bioactivity data with 4934 compounds. we conducted advanced filtering Which reduced the compunds number to 1498 compounds, after assesing the Lipniski's rule of five we found 1472 compounds among which 1352 are active compounds.

We also conducted extensive Exploratory data analysis to get idea about the filtered Bioactivity data (pIC50, negative logarithm of IC50)

### Part II

Here we are going to use the preprocessed data from Part I. Here we develop molecular descriptors data frames by using 4 different fingerprint types (pubchem, MACCCS, AtomPairs 2D count, AtomPairs 2D) and will be used in Part III and IIIB.

### PART IIIB
Prior to construction of the classication model, descriptors were subjected to mean centering and unit variance scaling as to afford comparability. Descriptors were removed if pairwise inter-correlation coefficients exceed the threshold value of 0.95 and correlation coefficient exceed the threshold value of 0.7. This resulted in reduced subsets consisting of 89 descriptors for PubChem.

In the construction of prediction models, the possibility of bias may arise from a single data split. In order to address this problem, Puzyn et al. suggested that prediction models should be constructed from N independent data splits. Thus, this study employs independent data splits using a split ratio of 70/30 where 70% of the entire data set was used as the internal set and the remaining 30% served as the external set. The nal prediction performance was obtained by calculating the mean and standard deviation values for statistical parameters from these independent data splits.





