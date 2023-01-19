# AI_Coursework
link to the **🍄 data**: https://archive.ics.uci.edu/ml/machine-learning-databases/mushroom/

link to notes - to be used in the final report: https://durhamuniversity-my.sharepoint.com/:w:/g/personal/sfvl24_durham_ac_uk/EW8i3oJJA-RGhpGEyMlw4RwBLH31PeuQ8WC486SgQk2gsg?e=Na09P2


## Data files:
### `mush.csv`
The **extended** dataset. It has not just first letters of attribute values, but them in full words => easier for us to read.


### `agaricus-lepiota.csv`
file to be used in training: agaricus-lepiota ----- the Data one


### `agaricus-lepiota-names.txt`
agaricus-lepiota ----- the Names one; contains credits and **some logical rules for the mushroom data sets**. Will be useful when checking if our AI is coming to right conclusions.

*Note: OR we can set those as initial guidelines if this is something we know how to do* :)


## Python notebook files
### `HelpSheet.ipynb`
the helpsheet from DurHack


### `main_code.ipynb`
the notebook used for rough workings
Currently main_code.ipynb will do this:
- load the dataset (extended version) into Pandas DF `dataset`
- creates count graphs for each attribute
- removes redundant attribute 'veil-type'
- replaces `'?'` with `NaN` for correct null detection
- removes attribute with null values
- performs a $\chi^2$ test on each attribute with edibility (concluding that no attribute is independent of edibility)
- creates cross tabulations between each attribute and edibility 
- Transforms data into numerical values.
- dataset `cleanDataset` contains only integer values, and has a shape of $(8416, 100)$
- Transforms data into numerical (values now in DF `cleanDataset`)
- Splits cleanDataset into X and y
- Performs PCA calculations on X to determine most useful attributes
- reduces X to a variable number of the most helpful attributes (10)
- splits data into `X_train`, `X_test`, `y_train`, `y_test` with variable ratios of train:test
- shuffles X and y so they can be used for Cross validation

- Copy of the logistic regression code from the slides

- K-nearest in a callable function using the X_train, y_train variables
