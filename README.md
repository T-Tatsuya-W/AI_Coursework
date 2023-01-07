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


### `workings.ipynb`
the notebook used for rough workings
Currently wokings.ipynb will do this:
- load the dataset (extended version) into Pandas DF `dataset`
- outputs the shape of `dataset`
- it prints counts of all the unique values from each attribute, as well as a count of null `NaN` values. 
- removes redundant attribute 'veil-type'
- replaces `'?'` with `NaN` for correct null detection
- removes attribute with null values
- performs a $chi^2$ test on each attribute with edibility (concluding that no attribute is independent of edibility)
- creates cross tabulations between each attribute and edibility 
- Transforms data into numerical values.

the clean dataset `cleanDataset` now only contains integer values, and has a shape of $(8416, 100)$
