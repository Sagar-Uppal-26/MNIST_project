# MNIST Digit Classification using ML

This project classifies handwritten digits from the [MNIST dataset](https://www.openml.org/d/554) using traditional machine learning models.

## 🚀 Overview

* Loaded MNIST dataset (`70,000` images, `784` features).
* Removed pixel columns always set to 0 (black).
* Scaled features using `StandardScaler`.
* Trained:

  * **Logistic Regression** → Accuracy: `0.92`, F1: `0.92`
  * **Random Forest** → Accuracy: `0.97`, F1: `0.97`
* Tuned Random Forest using `GridSearchCV` → same high performance.

## 🛠 Libraries

* Scikit-learn
* Pandas, NumPy
* Matplotlib, Seaborn (optional)

## 📈 Results

| Model               | Accuracy | F1 Score |
| ------------------- | -------- | -------- |
| Logistic Regression | 0.92     | 0.92     |
| Random Forest       | 0.97     | 0.97     |

✅ **Random Forest** performed best.

## 📂 How to Use

1. Load data with `fetch_openml`.
2. Preprocess & scale.
3. Train models & evaluate using classification report and confusion matrix.
4. (Optional) Tune with `GridSearchCV`.

## 📁 Dataset

* Source: [OpenML - MNIST](https://www.openml.org/d/554)
* Classes: 10 (digits 0–9)

## ✍️ Author

* **Sagar Uppal**
* GitHub: Sagar-Uppal-26(https://github.com/Sagar-Uppal-26)

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---
