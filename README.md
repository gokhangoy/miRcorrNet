# miRcorrNet
This tool allows you to make an integrated mRNA - miRNA profiles analysis. Via using this document you can easily execute the steps and you can obtain the results. Using this document you can easily repeat the experiments.

# Data Preparation
miRcorrNet uses 2 different data sheets with same control-case column. It means you should have same samples in one column which should be both in mRNA and miRNA data sheet. In this study we used KNIME analytics platform. Therefore, the data is stored in ".table" extension files.

# mRNA Data (Gene Expression)
In mRNA data one should have samples in the rows and gene names in the columns but the type of the genes should be double. The "class" column represents the sample whether control or case. The type of class column should be String and there can be only 2 classes. Below one can see the some chunk of the mRNA data.
 
 ![alt text](https://github.com/gokhangoy/miRcorrNet/blob/master/Data%20Graphics/README%20Figures/mRNA_Data.JPG)
 
# microRNA Data
In miRNA data one should have samples in the rows and microRNA names in the columns but the type of the genes should be String. The "class" column represents the sample whether control or case. The type of class column should be String and there can be only 2 classes. Below one can see the some chunk of the miRNA data.

 ![alt text](https://github.com/gokhangoy/miRcorrNet/blob/master/Data%20Graphics/README%20Figures/miRNA_Data.JPG)

# Set up Parameters

miRcorrNet allows you to set some parameter values. These parameters :
*Negative Correlation Value (Default :  -0.6)
*Positive Correlation Value (Default :  +1.0)
*Number of Iterations       (Default :  100)

To be able to change these parameters one need to use SetParameters node in the workflow.

# Usage of miRcorrNet

The only thing one should do is install KNIME Analytics platform. The workflow for miRcorrNet is available. One just download and import that workflow into KNIME.

# Solution Approach Steps
1- Import data and set the parameters
2- Normalize mRNA and miRNA expression data
3- Find Differentially Expressed mRNAs and miRNAs
4- Compute the Pearson correlation coeeficient between mRNAs and miRNAs in a pairwise manner
5- Detect mRNAs and miRNAs target groups
6- Rank the target gene groups
7- Test on top ranked clusters

![alt text](https://github.com/gokhangoy/miRcorrNet/blob/master/Data%20Graphics/README%20Figures/miRcorrNet_v2.jpg)
