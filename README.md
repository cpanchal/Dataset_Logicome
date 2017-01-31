# Dataset_Logicome
The file named as NewDisjointScaledBigdata.csv contains scaled gene expression data of the significant genes and we partition this data into training and validation for our further analysis. 

The partition into training and validation is done with the ratio of 60:40 and samples are choosen randomly.

We run the algorithm for 20 times and for each run we partition the data into training and validation. The zip files named as "Datasets#.zip" are the different sets of training and validation datasets used in different run.

The file Codes.zip, contains R codes to process data and to derive boolean signature from a selected subset. 
We have used R-Studio to write the code, please use selection run method to run the lines of the code. 
https://support.rstudio.com/hc/en-us/articles/200484448-Editing-and-Executing-Code

- To view the complete material, please check the link: https://drive.google.com/file/d/0B6zKM8axhJXuaGJzVWd1RWVfbTQ/view?usp=sharing

- The link has following material. The codes have file path for this folders.

DataProcessing.R
------------------
This R file uses following folders.
The folder : DataDownloaded
- All the data from GEO in .soft format will be downloaded in this folder. The will process the data to get the gene expression data and save it in the same folder. At this point the data contain probes-gene expression.
The folder : Aggregated
- In this folder all the processed data will be aggregated as gene expression using the median values computed for all the probes associated to the same gene.
The fodler: GEO2R data
- In this folder we save all the results derived from the GEO2R analysis.

BooleanSignature.R
------------------
This R script uses following folders.

The folder: MLR result
- The prepared data are loaded in this R script and results are stored in this folder. 
- The folder contains subfolder, Datasets and Results.
- The Datasets folder contains the training and validation data that we have used for our method.
- The Results folder contains the results in the form of subsets and accuracies. 
- From the results,  we pick a file, "NonBinarisedSubsetResult9" and choose a subset. In this case we choose subet of size 3.
- Go to the R script and paste this subset and run the code to generate boolean signature. 
- The boolean signature  for each category could be found in the folder also.
- We have used LogicFriday tool to minimize the derive signature.
