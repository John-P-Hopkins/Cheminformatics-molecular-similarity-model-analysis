# Regression Model Analysis of FDA Subset Data

## Introduction 
This project involves conducting a regression analysis on a subset of data obtained from ZINC15. The data contains information about the simplified molecular-input line-entry system (SMILES) of various chemical species. The goal of this analysis is to determine the best model for predicting the properties of these chemical species based on their SMILES strings.

## Data Cleaning and Pre-Processing

The following steps were carried out to prepare the data for analysis:

- Checked the validity of all SMILES strings according to the SMILES notation rules.
- Converted SMILES strings into a standardized form using canonicalization.
- Removed non-chemical characters or artifacts from SMILES strings.
- Generated fingerprints using the Morgan/Circular Fingerprint algorithm with a bit size of 1615.

## Exploratory Data Analysis

- Conducted Tanimoto Similarity analysis and generated a heatmap of the Similarity Matrix.
- Conducted t-SNE analysis to visualize the chemical species in a lower dimensional space.
- Conducted PCA and interpreted the results.


## Model Building and Evaluation

- Used the Pycaret package to conduct initial model comparison.
- The LightGBM algorithm was selected as the base model.
- The AdaBoost algorithm was used to create an ensemble of the LightGBM model.
- The model was tuned using cross-validation to test different combinations of hyperparameters.
- The performance of the model was evaluated based on R-squared, Root Mean Squared Error (RMSE), and Mean Absolute Percentage Error (MAPE).
- The model was finalized and saved.

## Results

- The LightGBM model was found to be the best performing model during the initial model comparison, with a RMSE of 0.0044 and an R-squared of 0.9515.
- The ensemble of LightGBM and AdaBoost improved the performance of the base model, with a RMSE of 0.0036 and an R-squared of 0.9663.
- The performance of the model was evaluated using 10-fold cross-validation, giving a mean RMSE score of 0.0042 and a mean R-squared score of 0.9569.

## Conclusion

The ensemble of LightGBM and AdaBoost algorithm was found to be the best performing model for predicting the properties of chemical species based on their SMILES strings. By reducing the RMSE score and increasing the R-squared score, this model provides more accurate predictions than the base model.

### References
- "Resources." DISI, . 9 Feb 2017, 18:30 UTC. 3 Sep 2023, 08:39 <http://wiki.docking.org/index.php?title=Resources&oldid=9919>.
- https://en.wikipedia.org/wiki/Simplified_molecular-input_line-entry_system
- https://en.wikipedia.org/wiki/ASCII
- https://oi.readthedocs.io/en/latest/bioinfo/mol_fp/ecfp.html
