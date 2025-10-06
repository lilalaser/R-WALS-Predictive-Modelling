# WALS Predictive Modelling

## 1. Overview
This project explores typological data from the World Atlas of Language Structures (WALS) (https://wals.info/), focusing on WALS feature 134A (Green and Blue), which describes how the colours Green and Blue are encoded across languages.  

The goal of the analysis is to investigate whether certain typological features can be used to predict the presence or absence of other linguistic features, specifically in relation to the distinction between Green and Blue.  

It is hypothesized that features 132A (Number of Non-Derived Basic Colour Categories) and 133A (Number of Basic Colour Categories) can be employed to predict the occurrence of separate words for Green and Blue in languages. In other words, the higher the number of colour categories, the more likely it is that Green and Blue are expressed in separate colour terms.  

To test this hypothesis, three decision trees are employed:
1. To investigate the relationship between Green and Blue and the number of basic colour categories  
2. To explore the relationship with the number of derived colour categories  
3. To examine the combined effects of both features  

---

## 2. Dataset

### 2.1 Source
The data used in this project is a reduced version of the WALS dataset, originally obtained from a university course platform and shared in the repository.  
The full WALS database can be accessed at https://wals.info/.

### 2.2 Dataset Structure
The dataset contains the following columns.  
A feature is a structural property of language that describes one aspect of cross-linguistic diversity.

- File: lists the corresponding chapter in WALS  
- ID: identifies the WALS feature and the language  
- Language_ID: contains the WALS codes of the investigated languages  
- Language_name: contains the names of the investigated languages  
- Parameter_ID: identifies the WALS feature  
- Parameter_name: contains the name of the WALS feature  
- Value: contains the values of the WALS features  
- Source: provides references  
- Comment: additional comments  

---

## 3. Analysis

### 3.1 Tools used in the Analysis
- Language: R  
- Packages: rpart, rpart.plot, dplyr, tidyr, ggplot2  

### 3.2 Structure of the Analysis
a. Selection of a linguistic feature of interest: WALS feature 134A (Green and Blue); construction of alternative hypotheses about what other linguistic features might predict its occurrence in a given language.  

b. Construction of three decision trees to predict the selected linguistic feature's value based on the relevant predictor variables identified in the previous step.  

c. Comparison of the models and summary of predictions regarding the relationship between the grammatical parameters under investigation.  

### 3.3 Key Findings
- Languages with a larger inventory of basic colour categories are more likely to have separate terms for Green and Blue. For languages with a smaller number of basic colour categories (3–4), there is a higher occurrence of a single term for both colours.  

- A larger number of non-derived colour categories increases the likelihood of a language having two distinct terms for Green and Blue. Languages with fewer non-derived colour categories (3–4.5) tend to use a combined term for the two colours rather than separate terms.  

- The combined model (basic + non-derived colour categories) shows similar results to Tree 2, indicating that both basic and non-derived colour categories are equally suited to predict the semantic distinction between Green and Blue.  

---

## 4. Installation and Usage

1. Clone this repository: https://github.com/lilalaser/R-WALS-Predictive-Modelling

2. Open the R script in RStudio or another R environment.

3. Load the data:

   - Run the script.
   - Use file.choose() to select the dataset .csv file when prompted.
   - The script will load and display basic summaries of the dataset.

---

## 5. Contact
For questions or contributions, please contact me through GitHub.
Thank you
