# Bioinformatics

#### OMICs DATA ######
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

#### Why do we need computational models for drug design and discovery?? #######

-To discern structure-activity relationship (SAR) of chemical library
-In vitro-data are limited, expensive and time consuming, laborious etc.
-Computational models can be quickly built to predict teh pharmacokinetics (ADME/T)  and 
bioactivity (inhibition or activation of target protein) of query compounds  
-Models can be used to repurpose existing FDA approved drugs for new therapeutic 
treatment

Data Science (Unstructured Data >> Structured data >> uncover patterns >> gain knowledge >> gain wisdom )

######### QSAR ##########

Quantitative structure– activity relationship (QSAR) is ligand-based approach in computational drug design for correlating the molecular features of a chemical library with their respective bioactivity

-Modeling is a mathematical modeling that seeks to discern the relationship between 
the chemical structure and their bioactivity
-The chemical structure is defined by a set of molecular descriptors that can account for local or 
global physicochemical properties
-local features, e.g. the number/presence of specific functional moities (molecular fingerprints)
-Global Features e.g. molecular weight, lipophilicity  
 
Part I - In this solubility prediction project we have reproduced the solubility results of compounds given by Delaney (2004), article is cited in the notebook file


Here we also create new QSAR model for Estrogen Receptor Alpha (CHEM206) inhibitory compounds, inspired by the following articles:
https://pubs.rsc.org/en/content/articlelanding/2018/ra/c7ra10979b

The expression of ERa is greatly increased in breast cancer cells and as such represents a promising therapeutic target for combating breast cancer
QSAR has been instrumental in shedding light on the molecular basis of bioactivity of interest by learning from past bioactivity data while also being amenable to extrapolating on the bioactivity of new compounds that are foreign to the trained data set

Part II - Here we retrieve the Bioactivity data (only IC50) for inhibitory compounds for ER-alpha (CHEMBL206)

###### here all the files have .json extension convert them to .ipynb then work on them ######
