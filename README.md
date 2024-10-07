# Sports Match Prediction Using Machine Learning

## Project Overview
This project implements a machine learning model to predict the outcomes of sports matches based on historical data. It utilizes various statistical features from football (soccer) match data, including goals scored, shots on target, and other relevant metrics, to classify the match results into three categories: Home Win (H), Draw (D), and Away Win (A). The model is built using a Random Forest Classifier, which is well-suited for classification tasks due to its robustness and interpretability.

## Features
- **Data Sources**: The model is trained using datasets for the 2020-2021 and 2021-2022 football seasons, along with a final dataset that consolidates previous data.
- **Selected Features**: The following features are used for prediction:
  - `FTHG`: Full-Time Home Goals
  - `FTAG`: Full-Time Away Goals
  - `HS`: Home Shots
  - `AS`: Away Shots
  - `HST`: Home Shots on Target
  - `AST`: Away Shots on Target
  - `HC`: Home Corners
  - `AC`: Away Corners
  - `HF`: Home Fouls
  - `AF`: Away Fouls
  - `HY`: Home Yellow Cards
  - `AY`: Away Yellow Cards
  - `HR`: Home Red Cards
  - `AR`: Away Red Cards

## Methodology
1. **Data Loading and Preprocessing**: 
   - The project reads multiple CSV files containing match data and combines them into a single DataFrame.
   - The relevant features are selected, and the target variable is encoded for model training.
   
2. **Model Training**: 
   - The dataset is split into training and testing sets (80/20 split).
   - A Random Forest Classifier is trained using the training set.
   - Predictions are made on the test set.

3. **Model Evaluation**: 
   - The model's performance is assessed using accuracy, log loss, and ROC-AUC score.
   - Feature importance is extracted to understand the contribution of each feature to the prediction.

## Results
- **Model Accuracy**: 99.74%
- **Log Loss**: 0.0278
- **ROC-AUC Score**: 1.0000

### Top 5 Most Important Features:
| Feature | Importance |
|---------|------------|
| FTHG    | 0.527675   |
| FTAG    | 0.338460   |
| AF      | 0.022121   |
| HF      | 0.021167   |
| AST     | 0.019101   |

## Usage
To run this project:
1. Clone the repository.
2. Ensure you have the necessary Python libraries installed (e.g., `pandas`, `numpy`, `scikit-learn`).
3. Update the `file_paths` in the `main()` function to point to your local CSV files containing the match data.
4. Execute the script to train the model and evaluate its performance.

## Future Work
- Experiment with other machine learning algorithms (e.g., XGBoost, Neural Networks) to potentially improve prediction accuracy.
- Expand the dataset with additional features or more seasons to increase the robustness of the model.
- Implement a web interface to allow users to input match statistics and get predictions.

## License
This project is licensed under the MIT License.
