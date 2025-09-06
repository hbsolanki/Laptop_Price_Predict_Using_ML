# 💻 Laptop Price Prediction

This project predicts **laptop prices** using machine learning, based on specifications such as **RAM, SSD, HDD, GPU, CPU rank + generation, operating system, and brand**.  
It uses a **Random Forest Regressor** to estimate prices from the dataset.

---

## 📌 Features
- Dataset: `laptopPrice.csv`
- Preprocessing:
  - Converted RAM, SSD, HDD, and GPU storage into numeric values
  - Extracted CPU generation (e.g., 10th, 11th Gen)
  - Created a `processor_score` combining **CPU rank** (Celeron, i3, i5, i7, i9, Ryzen) with **generation**
  - Handled missing values by replacing with `"Unknown"`
- Machine Learning:
  - **RandomForestRegressor** trained on processed features
  - Evaluated with **R² score**
- Custom input support for prediction

---

## 📂 Project Structure
├── LaptopPricePredict.ipynb # Jupyter notebook with all steps
├── laptopPrice.csv # Dataset file (not included here)
├── README.md # Project documentation


---

## ⚙️ Installation & Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/LaptopPricePredict.git
   cd LaptopPricePredict
2. Install dependencies:

  pip install pandas numpy scikit-learn matplotlib


3. Open the notebook:

  jupyter notebook LaptopPricePredict.ipynb

🚀 Usage

  Load the dataset (laptopPrice.csv) into the project directory.
  
  Run the notebook step by step:
  
  Preprocess the dataset
  
  Train the Random Forest model
  
  Evaluate results with R² score
  
  Use the trained model to predict prices for new laptop specs

📊 Example Prediction
  # Example laptop specification for prediction
  laptop_specs = {
      "brand": "Dell",
      "processor_brand": "Intel",
      "ram_gb": 16,
      "ssd": 512,
      "hdd": 0,
      "os": "Windows",
      "graphic_card_gb": 4,
      "processor_score": 54  # e.g., i7 5th gen
  }
  
  predicted_price = model.predict([list(laptop_specs.values())])
  print("💰 Predicted Laptop Price:", predicted_price)

📈 Results

  Model trained with Random Forest Regressor
  
  Evaluated using R² score
  
  Feature importance shows that CPU score, RAM, and SSD are the strongest predictors

🛠️ Technologies Used

  Python 🐍
  
  Pandas, NumPy
  
  Scikit-learn
  
  Matplotlib
