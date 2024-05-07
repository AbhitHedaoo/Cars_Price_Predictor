# **Cars Price Predictor**

**Overview** - The "Cars Price Predictor" project aims to predict the prices of used cars based on various features such as the car's make, model, year of manufacture, kilometers driven, and fuel type. This project utilizes machine learning techniques, specifically linear regression, to build a predictive model.

**Data** - The dataset used in this project is sourced from a CSV file named quikr_car.csv. The dataset contains information about used cars listed on an online marketplace, including details such as the car's name, company, year of manufacture, kilometers driven, fuel type, and price.

**Data Cleaning** - The data cleaning process involves several steps to ensure the quality and consistency of the dataset:
- Removal of non-numeric values in the 'year' column and conversion of the column to integer data type.
- Removal of entries with "Ask For Price" in the 'Price' column and conversion of the column to integer data type after removing commas.
- Extraction of numeric values from the 'kms_driven' column, removal of commas, and conversion to integer data type.
- Handling missing values in the 'fuel_type' column.
- Simplification of the 'name' column by extracting only the first three words.

The cleaned dataset is saved as Cleaned_car.csv for further analysis and model training.

# **Model**
**Data Preprocessing**
- One-hot encoding is applied to categorical features ('name', 'company', 'fuel_type') using OneHotEncoder.
- The column transformer is created to apply one-hot encoding to categorical features and keep the remaining columns unchanged.

**Model Training**
- The dataset is split into training and testing sets using the train_test_split function.
- Linear regression model is trained using the training data.
- A pipeline is created to streamline the data transformation and model training process.

**Model Evaluation**
- The trained model is evaluated using the R-squared (R2) score, which measures the goodness of fit of the model.
- The model performance is assessed by calculating the R2 score on the test data.

**Model Deployment**
- The trained model is saved using pickle as LinearRegressionModel.pkl.
- The saved model can be used for predicting car prices based on new input data.

**Credits** - This project is inspired by the tutorials provided by CampusX Youtube Channel.

