## 🚢 Titanic - Machine Learning from Disaster

This project is based on the Titanic survival prediction dataset from [Kaggle](https://www.kaggle.com/competitions/titanic/). The goal is to predict whether a passenger survived the Titanic shipwreck using machine learning models.

---

### 🧰 Tools Used

* **Python**
* **Jupyter Notebook** (via Anaconda)
* **Pandas**, **NumPy**
* **Matplotlib**, **Seaborn**
* **Scikit-learn** (StandardScaler, RandomForestClassifier, etc.)

---

### 📁 Project Structure

```
├── code.ipynb             # Main notebook with all steps
├── train.csv              # Training dataset (from Kaggle)
├── test.csv               # Test dataset (from Kaggle)
├── submission.csv         # Generated prediction file for submission
├── README.md              # This file
```

---

### ⚙️ How to Run the Project

1. **Install Anaconda** (if not already):
   [Download Anaconda](https://www.anaconda.com/products/distribution) → Follow installation instructions for your OS.

2. **Launch Jupyter Notebook:**

   ```bash
   anaconda-navigator
   ```

   * Or, open terminal/cmd and type:

     ```bash
     jupyter notebook
     ```

3. **Open the Notebook:**

   * Navigate to the folder containing `code.ipynb`.
   * Open `code.ipynb` and run all cells in order.

4. **Generate Submission File:**

   * Once you run the model and get predictions, a file named `submission.csv` will be generated in the same directory.
   * This file can be uploaded to [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic/) for evaluation.

---

### 📌 Notes

* If `submission.csv` gives a **PermissionError**, make sure:

  * You don't have it already open in Excel.
  * You have write permissions to the directory.
  * Use a different name like `submission_v2.csv`:

    ```python
    submission.to_csv("submission_v2.csv", index=False)
    ```

---

### 📊 Model Used

* **Random Forest Classifier**

  ```python
  rf_model = RandomForestClassifier(n_estimators=100, max_depth=5, random_state=42)
  ```

* **Feature Scaling** for `Age` and `Fare` using:

  ```python
  from sklearn.preprocessing import StandardScaler
  ```

---

### ✅ Result

* The model predicts survival (1) or not (0) for each passenger in the test set.
* You can iterate over multiple models and versions of the submission.

