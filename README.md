# Predicting-Molecule-Toxicity

Predicting the toxicity of molecules in different species is very important when designing a drug or material that can end up in the environment so that minimal damage is done to the ecosystem. There are several methods to represent and featurise molecules in addition to several learning methods that can be used for this problem. 

Here, two individual methods are shown. 

1. ANNs trained on molecular descriptors from the RDKit and Mordred descriptor libraries, and on Morgan Fingerprints. This is a different implementation to the ANN architecture used in the full_analysis notebook, with very similar accuracies.
2. A CNN trained on graph representations of the molecular structures. 

These methods are part of a larger study comparing different techniques for predicting molecular toxicity for comparision of prediction accuracy and computational efficiency. Lasso regression analysis, Random Forests and dimensionality reduction were used in the exploratory data analysis. This was to identify the top descriptors that explain molecular toxicity (highest weight) from the RDKit and Mordred chemical descriptor libraries. Random Forests, ANNs and a GCNN were then implemented to predict the toxicty of molecules, where the performances for different sets of input training data were compared. The different sets of input data included the full descriptor libraries in addition to the filtered descriptor sets containing only the top parameters from the different data analysis methods used. This comparison showed that the prediction models were still able to learn the relationship between the chemical structure of molecules and their toxicity, where they retained their high accuracy when using the smaller set of top descriptors. This has important implications when considering the computational efficiency of training the models for larger sets of training data containing more molecules for improving generalisability. 

The full study can be found in the file "full_analysis.ipynb".
