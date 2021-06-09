# CHEMBL DATABASE

**IC50 value** is the quantitative value which indicates how much of a drug is required to inhibit 50% of a biological organism, here SARS CoV-2. 

For our study we will consider the **pIC50 value** which is the negative log of the IC50 value when converted to molar.

## About the project

### Obective
In this project, I am going to predict the concentration of a drug i.e. pIC50 value required for 50% inhibition of the SARS CoV-2 virus based upon the existing Descriptor information.

### Database
The common dataset of the molecules have been taken from **ChEMBL Database- https://www.ebi.ac.uk/chembl/**. It is a manually curated datasbase of all bioactive molecules having drug-like properties.

### Brief walk through
First of all, raw database contained a lot of unwanted data about all sorts of potential target organisms so I had to clean it to make it suitable for our target organism i.e. SARS CoV-2. 

After that I classified the molecules into 3 different classes such as *Active, Intermediate and Inactive* based upon its action against the virus, later removing the *Intermediate* class. 

Since the molecules are represented according to standard IUPAC notation, I had to assign each of them a unique numerical identity for machine interpretation. This is done through **SMILES notation.** For this purpose, I have taken the help of **RDkit Library.** This library is used to identify each molecule based upon their molecular weight and other chemical properties and calculate their respective pIC50 value.

For modelling, I have used **Linear Regression** and **Random Forest Regression.** Using the molecule's Descriptor information and corresponding pIC50 value these models are trained and used for our prediction.

##### NOTE: To aid in understanding, I have added my own comment lines. 
