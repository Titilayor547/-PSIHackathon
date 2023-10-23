# Dataset README
This hackathon is presented by the North Carolina Plant Sciences Initiative and supported by Bayer Crop Sciences. Bayer Crop Sciences has provided the following datasets.


If you have any questions or require further clarification, please don't hesitate to reach out.


## Dataset Description

This dataset is a comprehensive collection of agricultural data collected from maize fields across the continental US, consisting of environmental data, phenotypical data, genomic data, and three predictor variables. Each data type is tagged with a prefix: `E_` for environmental data, `P_` for phenotypical data, `G_` for genomic data, and `y_` for the predictor variable.


## Data Split

The dataset is divided into training and testing data:

- **Training Data:** Participants of the hackathon are expected to use data from the years 2002-2007 to predict three key agricultural metrics for maize fields: Yield, Test Weight, and Moisture content in the year 2008. This training data includes records from 2002 to 2007 and is labeled accordingly.

- **Testing Data:** The testing data is associated with the year 2008. Participants will use their trained models to make predictions for this year.

## Files

- `train_merged_features.csv`: Contains the training data, including records from 2002 to 2007.
- `test_merged_features.csv`: Contains the testing data for the year 2008. This dataframe does not contain the predictor variable columns (`y_MST`, `y_TWT`, and `y_YLD_BE`) as they are held for scoring predictions.
- `development_training_set.csv`: Contains a subset of the training data for users to develop algorithms efficiently before applying them to the larger training set.
- `submission_template.csv`: Contains a template for submission and scoring inlcuding prediction columns (`y_MST`, `y_TWT`, and `y_YLD_BE`) and the unique identification lines (`cSH_LINE`, `LOC`, and `YEAR`).
- The folder `unmerged_files` contains the enviornmental, genomic, and phenotype data in their separate files. These are uncleaned and unmerged. They are pre-split into train and test for ease of use. The genomic data remains the same across each year and as such does not have a train/test split file.

## Data Tagging

- `E_`: Environmental data.
- `P_`: Phenotypical data.
- `G_`: Genomic data.
- `y_`: Predictor variables.

## Development Data

To facilitate the development of algorithms and models, we have created a smaller development dataset. This dataset contains 3000 randomly selected rows from the original dataset. Users are encouraged to use this development dataset during code development, as it offers quicker processing times to ensure that code works without errors or bugs. However, it's essential to keep in mind that the development dataset is a subset of the training data.

## Usage Guidelines

1. Begin by exploring the development dataset (`development_training_set.csv`) to develop and test your algorithms and models.
2. Ensure that your code works correctly with the development dataset before applying it to the training and testing datasets.
3. When ready, train your models using the entire training dataset (2002-2007) to create the most informed predictions for the testing data (2008).
4. Users will submit their predictions, as frequently as they choose, to the Kaggle competition space where they will be scored using an average `RMSE` metrics of the predictor variables (`y_MST`, `y_TWT`, and `y_YLD_BE`).

