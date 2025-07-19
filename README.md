# Grid Search for SVM Classification on Social Network Ads Dataset

This project demonstrates how to train and evaluate a Kernel SVM classifier on the "Social_Network_Ads.csv" dataset, including the use of k-Fold Cross Validation and Grid Search to optimize hyperparameters.

## 📊 Dataset

The dataset used is `Social_Network_Ads.csv`, which contains user information such as Age and Estimated Salary, along with a binary label indicating whether a user purchased a product.

### Features:
- Age
- Estimated Salary

### Target:
- Purchased (0 or 1)

## 🧠 Model

- **Classifier**: Support Vector Machine (SVM)
- **Kernel**: Radial Basis Function (RBF) and Linear (tuned via Grid Search)

## 🧪 Steps Performed

1. **Importing Libraries**  
   Libraries such as NumPy, pandas, matplotlib, and scikit-learn are used.

2. **Loading the Dataset**  
   Load and extract features (`X`) and target (`y`) from the CSV file.

3. **Data Preprocessing**  
   - Train-test split (75/25)
   - Standard scaling (feature normalization)

4. **Model Training**  
   - SVM with RBF kernel is trained on the training set.

5. **Model Evaluation**  
   - Accuracy and Confusion Matrix computed on the test set.
   - 10-fold cross-validation to evaluate model robustness.

6. **Hyperparameter Tuning with Grid Search**  
   Grid Search is used to find the best combination of:
   - `C`: [0.25, 0.5, 0.75, 1]
   - `kernel`: ['linear', 'rbf']
   - `gamma`: [0.1 to 0.9] (only for RBF kernel)

7. **Visualization**  
   - Decision boundaries for both training and test sets.

## 📈 Results

- **Accuracy (cross-validation)**: Printed to console
- **Best Parameters**: Printed via GridSearchCV

## 🖼️ Plots

- SVM decision boundary visualization for:
  - Training set
  - Test set

## 🛠️ Requirements

- Python 3.x
- NumPy
- pandas
- matplotlib
- scikit-learn

Install dependencies using:

```bash
pip install numpy pandas matplotlib scikit-learn
