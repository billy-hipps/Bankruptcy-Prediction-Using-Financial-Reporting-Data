# Bankruptcy Prediction Using Financial Data

This project was developed as part of an academic assignment and achieved a mark of 73%. The objective was to implement a machine learning approach to predict bankruptcy using financial data from Taiwanese companies. The project compares Logistic Regression and Balanced Bootstrap Aggregating methods to create reliable bankruptcy prediction models.

## Data Source

The dataset used in this project is sourced from the [Taiwanese Bankruptcy Prediction Dataset](https://archive.ics.uci.edu/dataset/572/taiwanese+bankruptcy+prediction) on the UCI Machine Learning Repository. It includes financial ratios from 6819 companies collected between 1999 and 2009.

## Motivation

Accurate bankruptcy prediction models are crucial for governments, financial institutions, and small-scale lenders to assess economic activity and minimize credit risks. This project aims to develop robust models using machine learning techniques to improve upon traditional statistical methods.

## Project Structure

- `data/`: Contains the dataset and any preprocessed data files.
- `README.md`: Project overview and instructions.

## Installation

To run this project, you will need Python 3.8 and the following libraries:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn imbalanced-learn
```

## Usage

1. **Data Preprocessing:**
   - Load the dataset and preprocess it by handling missing values, scaling features, and performing feature selection.

2. **Model Training:**
   - Train a Logistic Regression model with Stratified Cross Validation (SCV).
   - Train a Balanced Bootstrap Aggregating (BB) model using Logistic Regression as the base learner.

3. **Model Evaluation:**
   - Evaluate the models using F1-score, ROC-AUC, precision, and recall metrics.
   - Compare the performance of the SCV Logistic Regression and Balanced BAgging models.

## Results

The models were evaluated on their ability to predict bankruptcy. Here are some key findings:

- **Logistic Regression (SCV):**
  - F1 Score: 0.27
  - ROC-AUC: 0.91
  - Precision: 0.16
  - Recall: 0.82

- **Balanced Bootstrap Aggregating (BB):**
  - F1 Score: 0.27
  - ROC-AUC: 0.92
  - Precision: 0.16
  - Recall: 0.82

Both models show good discrimination between classes, with high recall indicating effective capture of positive bankruptcy cases. However, precision is low, suggesting positive predictions are less reliable.

## Conclusion

This project demonstrates the challenges of predicting bankruptcy in an imbalanced dataset where successful businesses significantly outnumber unsuccessful ones. The Logistic Regression model with SCV performed marginally better than the Balanced BAgging model. Future improvements could include incorporating more diverse data and creating sector-specific models.

## References

- Altman, E.I. (1968). Financial Ratios, Discriminant Analysis and the Prediction of Corporate Bankruptcy. *The Journal of Finance*.
- Gnip, P., and Drotar, P. (2019). Ensemble methods for strongly imbalanced data: bankruptcy prediction. *IEEE Conference Publication*.
- Hackeling, G. (2017). Mastering Machine Learning with scikit-learn - Second Edition. Packt Publishing.