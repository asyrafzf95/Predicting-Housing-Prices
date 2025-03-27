# California Housing Price Prediction
This project involves predicting housing prices in California based on various features like location, population, and median income. The dataset used is from Kaggle's California Housing Prices.
The machine learning model chosen for this task is Gradient Boosting Regressor, which provides the best performance with the lowest validation error compared to other models like Linear Regression, K-Nearest Neighbors, and Random Forest.

## Project Setup
### Prerequisites
Python packages installed:
- pandas
- numpy
- sklearn
- kaggle (for dataset access)

### Getting Started
1. Install dependencies:

Create a virtual environment and install the required dependencies:
```
pip install -r requirements.txt
```
2. Set up Kaggle API credentials:
To access the dataset from Kaggle, you need to authenticate using the Kaggle API. Place your kaggle.json (which you can download from here) in the .kaggle directory in your home folder.
```
mkdir ~/.kaggle
cp kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json
```
3.Download the dataset:
I used the Kaggle API to download the dataset directly:
```
kaggle datasets download -d camnugent/california-housing-prices
unzip california-housing-prices.zip
```
4. Run the notebook:
All code is available in the Jupyter notebook format. You can run it to train and evaluate the Gradient Boosting model, along with other models.

## Data Preprocessing
- Data Cleaning: Rows with missing values were dropped.
- Feature Engineering: One-hot encoding was applied to the 'ocean_proximity' column.
- Feature Scaling: The first 8 columns were scaled using StandardScaler to improve model performance.

## Model Training
Models Evaluated:
1. Linear Regression
- Training RMSE: 68593.06
- Validation RMSE: 71382.44
2. K-Nearest Neighbors Regressor
- Training RMSE: 53759.10
- Validation RMSE: 62161.23
3. Random Forest Regressor
- Training RMSE: 43519.22
- Validation RMSE: 53295.31
4. Gradient Boosting Regressor (Chosen Model)
- Training RMSE: 47274.82
- Validation RMSE: 51414.90

## Conclusion
The Gradient Boosting Regressor model outperforms the others in terms of both training and validation RMSE, and it has been selected as the final model for this task.

## File Structure
- housing.csv: The dataset containing housing data.
- Predictiong Housing Prices.ipynb: Jupyter notebook for the entire data processing, model training, and evaluation pipeline.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
