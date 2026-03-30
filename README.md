# 🧠 AI Smart Categorizer & Expense Tracker

An AI-powered module designed to be integrated into an Android (Kotlin) Expense Tracker app. This project focuses on automating manual tasks for users, such as categorizing expenses and (coming soon) scanning receipts.

---

## 🚀 Current Feature: Smart Categorizer

Instead of manually selecting "Food," "Transport," or "Rent," the user simply types a note (e.g., *"Uber to airport"* or *"Netflix subscription"*). The AI instantly predicts and selects the correct category.

### **Technical Breakdown**
- **Model**: Linear Support Vector Machine (LinearSVC)
- **Vectorization**: TF-IDF (Term Frequency-Inverse Document Frequency)
- **Accuracy**: **90% – 93%** 🔥
- **Categories**: Food, Travel, Rent, Utilities, Entertainment, Health, Education, Shopping, and Income.
- **Robustness**: High-precision keyword mapping and synthetic data augmentation used to handle noisy real-world data.

### **How to Use (Jupyter Notebook)**
The complete training and verification pipeline is available in **`expense.ipynb`**. You can run the notebook to:
1. Load the finance datasets.
2. Clean and normalize transaction notes.
3. Train the SVM model.
4. Verify the model with custom test cases.

---

## 🛠 Upcoming Feature: Receipt Scanner 📸

The next evolution of this project is a **Computer Vision + NLP** Receipt Scanner that eliminates manual entry entirely.

### **What it does:**
1. User captures an image of a grocery or retail receipt.
2. The app automatically extracts the **Total Amount**, **Date**, and **Store Name**.
3. The `AddExpenseScreen` is pre-filled, requiring only a single tap to save.

### **The Tech Stack:**
- **OCR Engine**: Google's ML Kit (Offline capability for fast processing).
- **NER Model**: A custom **Named Entity Recognition (NER)** model to scan the extracted text and identify entities (Merchant Name, Amount, Date).
- **Integration**: Will be fully connected to the existing **Expense Tracker Kotlin app** for a seamless mobile experience.

---

## 📂 Project Structure
- `expense.ipynb`: Main Jupyter Notebook for model development.
- `budgetwise_finance_dataset.csv`: Training data for the categorizer.
- `categorizer_model.pkl`: Exported SVM model for inference.
- `vectorizer.pkl`: Exported TF-IDF vectorizer.
- `.gitignore`: Configured to protect model files and caches from being tracked.

---

## 🤝 Integration
This module is designed to work in tandem with the **[Allinone Expense Tracker](https://github.com/Basanagouda25/AI_Expense_Categorizer)** (Kotlin). The `.pkl` models generated here are optimized for conversion to lightweight formats suitable for mobile deployment.

---

### **Maintainer**
Developed with ❤️ by **[Basanagouda25](https://github.com/Basanagouda25)**.
