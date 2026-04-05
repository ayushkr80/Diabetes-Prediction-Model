🩺 Diabetes Prediction Model (SVM-Based)

📌 Overview
This project builds a Diabetes Prediction System using a Support Vector Machine (SVM) model.
It predicts whether a person is diabetic based on medical parameters.

The workflow includes:

Data preprocessing
Feature standardization
Model training (SVM)
Accuracy evaluation
Real-time prediction system
🧠 Model Used
✅ Support Vector Machine (SVM)
Kernel: linear
Library: sklearn.svm.SVC
📂 Project Structure
Diabetes-Prediction/
│── Diabetes_prediction_model.ipynb   # Main ML notebook
│── diabetes.csv                      # Dataset
│── README.md                         # Documentation
📊 Dataset Details

The dataset contains the following features:

Feature	Description
Pregnancies	Number of times pregnant
Glucose	Blood sugar level
BloodPressure	Blood pressure
SkinThickness	Skin fold thickness
Insulin	Insulin level
BMI	Body Mass Index
DiabetesPedigreeFunction	Genetic influence
Age	Age of patient

🎯 Target Variable:

0 → Non-Diabetic
1 → Diabetic
⚙️ Workflow
1️⃣ Data Collection
diabetes_dataset = pd.read_csv('diabetes.csv')
2️⃣ Data Analysis
Shape of dataset
Statistical summary (describe())
Class distribution (value_counts())
3️⃣ Feature & Label Split
X = diabetes_dataset.drop(columns='Outcome', axis=1)
Y = diabetes_dataset['Outcome']
4️⃣ Data Standardization
scaler = StandardScaler()
scaler.fit(X)
X = scaler.transform(X)

👉 Important: Standardization improves SVM performance.

5️⃣ Train-Test Split
X_train, X_test, Y_train, Y_test = train_test_split(
    X, Y, test_size=0.2, stratify=Y, random_state=2
)
6️⃣ Model Training
classifier = svm.SVC(kernel='linear')
classifier.fit(X_train, Y_train)
7️⃣ Model Evaluation
Training Accuracy
Test Accuracy
accuracy_score(Y_test, X_test_prediction)
📈 Results
✔️ Training Accuracy: High
✔️ Test Accuracy: Good generalization

(Exact values depend on dataset run)

🔮 Prediction System

Example input:

input_data = (5,166,72,19,175,25.8,0.587,51)

Steps:

Convert to NumPy array
Reshape
Standardize
Predict

Output:

Prediction: Diabetic / Non-Diabetic
🛠️ Tech Stack
Python 🐍
NumPy
Pandas
Scikit-learn
📊 Visual Workflow
Dataset → Preprocessing → Standardization → Train/Test Split
        → SVM Model → Evaluation → Prediction
🚀 How to Run
1️⃣ Clone Repo
git clone https://github.com/your-username/diabetes-prediction.git
cd diabetes-prediction
2️⃣ Install Dependencies
pip install numpy pandas scikit-learn
3️⃣ Run Notebook
jupyter notebook
🎯 Future Improvements
🔥 Deploy using Streamlit (HIGHLY recommended for internships)
📊 Add visualization dashboard
⚡ Try other models (Random Forest, XGBoost)
🧠 Hyperparameter tuning
🤝 Contributing

Pull requests are welcome!
Feel free to fork and improve 🚀

👨‍💻 Author

Ayush Kumar
IIT Bhilai

⭐ If you like this project

Give it a star ⭐ on GitHub — helps a lot in internships!
