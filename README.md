
# Stellar Classification Dataset - SDSS17

## Overview

This project aims to classify stars, galaxies, and quasars based on their spectral characteristics using the Stellar Classification Dataset from the Sloan Digital Sky Survey DR17. Multiple machine learning classifiers were tested with various parameters to determine the most accurate model. The final model achieved an accuracy of 98%.

## Dataset

The dataset consists of 100,000 observations of space taken by the SDSS. Each observation is described by 17 feature columns and 1 class column, which identifies whether the object is a star, galaxy, or quasar.

### Features:
1. **obj_ID**: Object Identifier
2. **alpha**: Right Ascension angle (at J2000 epoch)
3. **delta**: Declination angle (at J2000 epoch)
4. **u**: Ultraviolet filter in the photometric system
5. **g**: Green filter in the photometric system
6. **r**: Red filter in the photometric system
7. **i**: Near Infrared filter in the photometric system
8. **z**: Infrared filter in the photometric system
9. **run_ID**: Run Number used to identify the specific scan
10. **rerun_ID**: Rerun Number to specify how the data was processed
11. **cam_col**: Camera column to identify the camera used
12. **field_ID**: Field number to identify the field
13. **spec_obj_ID**: Object Identifier for spectroscopy
14. **class**: Object class (Star, Galaxy, Quasar)
15. **redshift**: Redshift value of the object
16. **plate**: Plate ID for spectroscopy
17. **mjd**: Modified Julian Date for spectroscopy
18. **fiber_ID**: Fiber ID for spectroscopy

## Methodology

### Data Preprocessing
1. **Data Cleaning**: Removed any rows with missing or inconsistent values.
2. **Feature Scaling**: Applied standardization to ensure that the features have a mean of 0 and a standard deviation of 1.
3. **Train-Test Split**: Split the data into training (80%) and testing (20%) sets.

### Model Selection
Multiple classifiers were tested, including:
1. **Logistic Regression**
2. **Random Forest**
3. **K-Nearest Neighbors (KNN)**
4. **Gradient Boosting**

Each classifier was fine-tuned using Grid Search and Cross-Validation to find the optimal hyperparameters.

### Best Model
{'bootstrap': True,
 'ccp_alpha': 0.0,
 'class_weight': None,
 'criterion': 'gini',
 'max_depth': None,
 'max_features': 'sqrt',
 'max_leaf_nodes': None,
 'max_samples': None,
 'min_impurity_decrease': 0.0,
 'min_samples_leaf': 1,
 'min_samples_split': 2,
 'min_weight_fraction_leaf': 0.0,
 'n_estimators': 500,
 'n_jobs': None,
 'oob_score': False,
 'random_state': None,
 'verbose': 0,
 'warm_start': False}
This model achieved an accuracy of 98% on the test set.


### Confusion Matrix
The confusion matrix showed excellent performance in distinguishing between stars, galaxies, and quasars.

## Conclusion

The project successfully classified celestial objects with high accuracy. The Random Forest classifier proved to be the most effective model for this task. Future work could explore additional features or more advanced models to further improve classification performance.

## Installation and Usage

1. **Clone the repository**:
    ```bash
    git clone 'the link'
    ```
2. **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```
3. **Run the classification script**:
    ```bash
    python classify.py
    ```

## Acknowledgements

- The Sloan Digital Sky Survey (SDSS) for providing the dataset.
- Contributors and maintainers of the machine learning libraries used.

---

This README file provides a comprehensive overview of the project, including dataset details, methodology, results, and instructions for installation and usage.
