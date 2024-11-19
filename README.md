# Kickstarter Success Prediction

Empowering investors and founders with data-driven insights.

## Overview
This project aims to assist Kickstarter founders and investors in making informed decisions using machine learning. By analyzing patterns from past campaigns, we provide predictions on the likelihood of success, minimizing financial risk and uncertainty.

## Features
- **Dataset**: Contains 200,000 Kickstarter campaigns (successful, failed, canceled, suspended, and live) from 2009-2018. Extensive preprocessing ensured quality and usability of data.
- **Machine Learning Models**:
  - Logistic Regression
  - k-Nearest Neighbors (KNN)
  - Random Forest
- **Best Model**: KNN with Manhattan distance and 14 neighbors achieved an accuracy of 77.5%.

## Key Insights
1. **Successful Countries**: Hong Kong (70%) and Luxembourg (66%) have the highest success rates. The US leads in the total number of successful projects.
2. **Promising Categories**: Top categories include Product Design, Tabletop Games, and Software.
3. **Timing**: Timing has minimal effect on success, though fewer projects are launched in December.

## Methodology
### Data Preprocessing
- Removed irrelevant columns (e.g., location, permissions).
- Transformed categorical variables into numerical ones using encoding techniques.
- Balanced classes to ensure fair model training.

### Feature Engineering
- Created new features like `amount_per_backer` and `marketing_mix` from raw data.
- Converted time-based features into usable formats.

### Models
- **Logistic Regression**:
  - Explored different regularization parameters using GridSearchCV.
- **k-Nearest Neighbors (KNN)**:
  - Tuned hyperparameters like number of neighbors, distance metrics, and weight functions.
- **Random Forest**:
  - Evaluated feature importance and optimized hyperparameters for better prediction.

## Results
| Model            | Accuracy | Key Features                        |
|-------------------|----------|-------------------------------------|
| Logistic Regression | ~76%     | Scaled features, optimized with GridSearch |
| KNN               | 77.5%    | `fundraising goal`, `category`, `country` |
| Random Forest     | ~75%     | Feature importance visualization |

### Example Findings
- Successful campaigns often fall in popular categories and are better marketed using features like "Staff Pick".
- Low fundraising goals have higher chances of success.

## Recommendations
- If a project is predicted to fail:
  1. Adjust the fundraising goal.
  2. Invest in marketing features like "Staff Pick".
  3. Select more promising categories.

## Future Work
1. **Live Campaign Predictions**: Use live projects as unseen data for prediction.
2. **Seasonal Trends**: Tailor recommendations for seasonal products.
3. **Investor ROI Predictions**: Add financial metrics to assess return on investment.

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/username/repo.git
   ```
2. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebooks:
   - [ML Project Kickstarter.ipynb](./ML-project-Kickstarter.ipynb)
   - [Logistic Regression.ipynb](./ML_Project_LR.ipynb)
   - [Random Forest.ipynb](./random_forest.ipynb)

4. Visualize results and use the trained models for predictions.

## Contributing
Contributions are welcome! Feel free to fork the repository and submit a pull request.

## License
[MIT License](LICENSE)

