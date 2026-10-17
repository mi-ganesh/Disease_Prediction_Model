# Disease Prediction Model Using Machine Learning

## About the Project

This project predicts possible diseases based on symptoms using machine learning. It uses a Random Forest classifier trained on a disease–symptom dataset to identify patterns and generate disease predictions.

The project also includes hyperparameter tuning and an entropy-based adaptive questioning approach to select relevant follow-up symptom questions.

## Features

- Disease prediction based on symptoms
- Random Forest classification
- Hyperparameter tuning using RandomizedSearchCV
- Top 3 predicted diseases with probability estimates
- Model evaluation using accuracy, precision, recall, and F1-score
- Symptom feature importance analysis
- Entropy-based uncertainty measurement
- Adaptive symptom questioning using estimated information gain
- Support for confirmed, denied, and unknown symptoms

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- SciPy
- Joblib

## Dataset

The model uses a disease–symptom dataset containing symptom features and corresponding disease labels.

The dataset is preprocessed, disease labels are encoded, and the data is divided into training and testing sets. Partially observed training examples are also used to support the adaptive symptom-questioning workflow.

**Note:** The dataset is not included in this repository. Ensure that you have permission to use it and update the dataset path in the notebook before running the project.

## Machine Learning Approach

### Random Forest Classifier

Random Forest combines multiple decision trees to predict disease classes based on symptom patterns. It is used as the primary classification algorithm.

### Hyperparameter Tuning

RandomizedSearchCV is used to explore different Random Forest hyperparameters and select a configuration based on cross-validation performance.

### Entropy-Based Adaptive Questioning

Entropy measures uncertainty in the model's predicted disease probabilities. The system estimates the information gain of candidate symptom questions and selects the question expected to reduce uncertainty the most.

### Model Evaluation

The model is evaluated using:

- **Accuracy:** Overall proportion of correct predictions.
- **Precision:** Proportion of predicted cases for a class that are correct.
- **Recall:** Proportion of actual cases for a class that are correctly identified.
- **F1-score:** Harmonic mean of precision and recall.

## Project Structure

```text
.
├── disease_prediction_model_finetuned.ipynb
└── README.md
```

## Installation

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib scikit-learn scipy joblib
```

## How to Run

1. Clone or download the repository.
2. Download the required dataset separately and place it in the appropriate directory.
3. Open `disease_prediction_model_finetuned.ipynb` in Jupyter Notebook or Google Colab.
4. Update the dataset path if necessary.
5. Install the required dependencies.
6. Run the notebook cells in order.
7. Review the model evaluation metrics and test the prediction workflow.

## Applications

- Educational machine learning projects
- Disease classification experiments
- Symptom-based prediction research
- Adaptive questioning and information-gain experiments

## Limitations

- Performance depends on the quality and representativeness of the dataset.
- Hyperparameter tuning does not guarantee improved performance on unseen data.
- Predicted probabilities are not necessarily calibrated clinical probabilities.
- Entropy-based question selection is an estimated heuristic and is not a clinically validated diagnostic method.
- This project is intended for educational and research purposes and must not replace professional medical advice or diagnosis.

## Future Improvements

- Evaluate the model on independent datasets.
- Improve probability calibration and class-wise performance.
- Develop a user interface for symptom input.
- Integrate additional validated data sources.
- Explore further model optimization and interpretability methods.

## License

Add an appropriate license before distributing or reusing this project. Follow the dataset provider's terms and conditions.
