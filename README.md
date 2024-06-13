# Species Genome Analysis and Animal Group Predictor

## Overview

This project performs species genome analysis and group prediction using genome sequences from various species. The analysis includes extracting DNA sequences, gene names, and protein descriptions, and comparing genomic information across species. It also involves predicting the species of unknown genomes using machine learning techniques.

## Functionality

### Parsing Genome Files

The script parses genome files in FASTA format, extracting sequences, gene names, and protein descriptions for each species. It creates dataframes for each species containing this information. Supported species include:

- Human
- Chicken
- Atlantic Salmon
- Common Lizard
- Common Frog

### Combining and Analyzing Data

All species-specific dataframes are combined into a single dataframe for comprehensive analysis. The combined dataframe is used to compare the sequence lengths across different species and to analyze the frequency of various trimers (3-mer sequences).

### K-mer Transformation

The DNA sequences are transformed into K-mer representations (subsequences of length 3) using a `KMerTransformer`. The transformed data is used to create a feature matrix for machine learning models.

### Correlation Analysis

The correlation between different trimers is visualized using a heatmap, revealing high correlations between many codons. This helps in understanding the underlying patterns in the genomic data.

### Statistical Analysis

The mean and standard deviation of each codon across different species are calculated and visualized. This helps in identifying unique genomic characteristics of each species.

### Machine Learning Model

A machine learning pipeline is constructed using K-mer and K-group transformations, scaling, and an ExtraTreesClassifier. The model is trained to predict the species of a given DNA sequence.

### Model Evaluation

The model's performance is evaluated using classification reports, showing precision, recall, and F1-scores for each species. Visualization tools such as classification reports, class prediction errors, and ROC-AUC curves are used to illustrate the model's accuracy and prediction errors.

### Animal Group Prediction

The project also includes predicting the animal group (e.g., vertebrates, invertebrates) using the genomic data. A heatmap visualization shows the distribution of predicted groups across different species.

### Mystery Genome Analysis

Two mystery genomes are analyzed to predict their species. The genomic data of the mystery genomes are compared with known species to identify their closest matches.

## Summary of Steps

1. **Import Genomic Data**: Genomic sequences are imported and parsed from FASTA files.
2. **Create Dataframes**: Dataframes are created for each species with sequences, gene names, and protein descriptions.
3. **Combine Dataframes**: All species dataframes are combined into one for comparative analysis.
4. **K-mer Transformation**: DNA sequences are transformed into K-mer representations.
5. **Correlation Analysis**: Correlation between different trimers is analyzed and visualized.
6. **Statistical Analysis**: Mean and standard deviation of codon frequencies are calculated and visualized.
7. **Model Training**: A machine learning model is trained to classify the species based on genomic data.
8. **Model Evaluation**: The model is evaluated using classification reports and visualizations.
9. **Animal Group Prediction**: The animal group for each species is predicted and visualized.
10. **Mystery Genome Analysis**: The species of two mystery genomes are predicted by comparing their genomic data with known species.

This project provides a comprehensive framework for analyzing and predicting species using genomic data, leveraging advanced data processing and machine learning techniques.

Steven Rud

Credit to https://github.com/rollingstorms/DNA-Sequence-Classification/blob/main/src/KMerTransformers.py for the KMer Transformers library and code inspiration.
