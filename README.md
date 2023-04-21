# product_type

## Goal

Predict if an item listed in the marketplace is **new or used**.

## Folders

- *src/outputs* <> Contains the results from the data processing performed in the Data Wrangling & EDA steps.
- *src/renders* <> Contains .ipynb codes exported as HTML for viewing.

## Files

- *dwr.ipynb* <> Processing and treatment of raw data;
- *eda.ipynb* <> Analyzes carried out to explore the *eda_new_or_used.parquet* dataset;
- *model.ipynb* <> All processes used for training and evaluating the Machine Learning model;
- *new_or_used.py* <> Function provided for reading the json data;
- *requirements_{step}.txt* <> Application dependencies and their used versions from each .ipynb.

## Summary

First, the data provided were read and treated at the line and column level to assist the exploratory data analysis step (>>**dwr.ipynb**<<). The data cleaning part was focused on ensuring the presence of discriminating variables (*not missing/inconsistent values*) and the stability of important criteria for modeling (*temporal distribution over product creation date and confirmation of only 2 classes for the 'condition'*);

Afterwards, all the data analysis to generate insights and manipulate the features that would compose the Machine Learning model (>>**eda.ipynb**<<). We verified the **main variables** for the composition of the model, relating its **percentage with the target** and we explored a lot the **text features** (*'warranty'* & *'title'*), which presented a LOT OF DISCRIMINATION TO CLASSIFY THE TARGET of certain words when they existed;

And finally, implementation of techniques for **training and evaluating** the results of the predictions of the final model (>>**model.ipynb**<<). The objective was to achieve an **Accuracy result of 86%** and a high percentage of **Precision** was chosen as a secondary metric, in line with the approach mentioned in *dwr.ipynb*: Using variables *previously related to the publication of the product on the marketplace to avoid false positives*. The result obtained for the second metric was **89%**, considered satisfactory.

## For better understanding

Read the exported HTML, where each method is explained and implemented, as follows:

1 - **dwr.ipynb**; \
2 - **eda.ipynb**; \
3 - **model.ipynb**
