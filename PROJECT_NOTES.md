# Portfolio cleanup notes

Key technical changes from the laboratory version:

- Created explicit train/validation/test splits.
- Removed SVM hyperparameter selection on the final test set.
- Removed Decision Tree `ccp_alpha` selection on the final test set.
- Replaced ANN early stopping on test accuracy with validation-based early stopping.
- Restored the best ANN weights after early stopping.
- Fixed inconsistent binary-class labels by deriving the most-confused pair from validation predictions.
- Fixed outlier scaling so predictions use a scaler learned from training data.
- Kept the same untouched test set when comparing models trained with and without outliers.
- Consolidated duplicated ANN definitions/training code.
- Added fixed random seeds, clear sectioning, reusable helpers, and portfolio-facing documentation.
