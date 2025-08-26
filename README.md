# MNIST Digit Classification using Machine Learning

This project focuses on classifying handwritten digits from the [MNIST dataset](https://www.openml.org/d/554) using traditional machine learning algorithms. The dataset contains **70,000 grayscale images** of handwritten digits (0–9), each represented as a **784-dimensional vector** (28x28 pixels).

## 📌 Project Overview

* Data fetched using `fetch_openml` from `sklearn.datasets`.
* Combined features and target into a single DataFrame.
* Preprocessing included removing features (pixels) that always have a value of 0 (i.e., always black).
* Scaled remaining features using `StandardScaler` within a `ColumnTransformer`.
* Trained two machine learning models:

  * **Logistic Regression**
  * **Random Forest Classifier**
* Evaluated both models using classification report and confusion matrix.
* Tuned the best-performing model (Random Forest) using `GridSearchCV`.

---

## ⚙️ Technologies & Libraries Used

* Python
* Scikit-learn
* Pandas
* NumPy
* Matplotlib (optional for visualization)
* Seaborn (optional for confusion matrix heatmap)

---

## 📊 Results

| Model                 | Accuracy | F1 Score |
| --------------------- | -------- | -------- |
| Logistic Regression   | 0.92     | 0.92     |
| Random Forest         | 0.97     | 0.97     |
| Random Forest (Tuned) | 0.97     | 0.97     |

**Conclusion**: The Random Forest Classifier outperforms Logistic Regression on this dataset, even before hyperparameter tuning.

---

## 🧠 Steps Performed

1. **Data Loading**:

   ```python
   from sklearn.datasets import fetch_openml
   mnist = fetch_openml('mnist_784', version=1, as_frame=False)
   X, y = mnist["data"], mnist["target"]
   ```

2. **Data Preprocessing**:

   * Created a combined DataFrame of features and target.
   * Removed columns where all values were zero (black pixels).
   * Split the data into training and testing sets.
   * Scaled the remaining features using `StandardScaler`.

3. **Model Training & Evaluation**:

   * Trained Logistic Regression and Random Forest.
   * Compared their performance using:

     * `classification_report`
     * `confusion_matrix`

4. **Hyperparameter Tuning**:

   * Used `GridSearchCV` to find the best parameters for Random Forest.
   * Retrained the model with best parameters and achieved the same high performance.

---

## 🗃️ Dataset

* **Name**: MNIST (via OpenML)
* **Source**: [`mnist_784`](https://www.openml.org/d/554)
* **Shape**: `(70000, 784)` features and `70000` labels
* **Classes**: 10 (digits from 0 to 9)

---

## 📁 How to Use This Project

1. Clone or download this repository.
2. Open the Python file or Jupyter notebook.
3. Run the code step-by-step to:

   * Load and preprocess data
   * Train the models
   * Evaluate results

---

## ✍️ Author

* **Sagar Uppal**
* GitHub: Sagar-Uppal-26(https://github.com/Sagar-Uppal-26)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
