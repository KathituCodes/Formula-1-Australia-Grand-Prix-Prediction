# 🏎️ Formula-1-Australia-Grand-Prix-Prediction

## 🏁 Overview
As a passionate F1 fan closely following the 2025 season, I wanted to explore the art of race prediction. This project leverages machine learning to estimate Formula 1 race standings by analyzing key performance indicators like:

- **Qualifying Performance**
- **Past Race Performance**
- **Starting Grid Position**

By combining these factors, the model predicts overall race times for the **2025 Australian Grand Prix**, offering insights into potential final standings. Built using **Python, FastF1 API, and Scikit-Learn**, this project focuses on predicting race lap times.

---

## 📊 Data Collection (FastF1 API)
To build an accurate model, we extracted historical race and qualifying data from the **2024 season**, using the **FastF1 API** to retrieve:

- **Lap times** for all drivers in the **2024 Australian GP**
- **Grid positions** from the **2024 season**
- **Simulated qualifying times** for the **2025 Australian GP** (used for model testing)

---

## 🔍 Feature Engineering
The model’s predictions rely on carefully selected features:

- **2024 Lap Times** – Provides historical context for each driver’s race pace.
- **2025 Qualifying Times** – Acts as an initial performance benchmark.
- **Grid Position** – Captures race start advantage and overtaking difficulty.

While this version does not yet account for **fuel loads, pit strategy, or weather conditions**, future iterations will incorporate these elements for even better accuracy.

---

## 🤖 Model Selection
The **Gradient Boosting Regressor** (Scikit-Learn) was chosen because:

- It handles **non-linear dependencies** well, ideal for structured race data.
- It can capture **complex relationships** between qualifying performance and race pace.
- It performs reliably with **small datasets**, a necessity given F1’s limited race history per season.

**Model Evaluation:**
- The **Mean Absolute Error (MAE)** is **3.47 seconds**, meaning the predicted lap times deviate on average by 3.47 seconds from actual times. While this is a solid starting point, milliseconds matter in F1, and refining accuracy is essential.

---

## 🚧 Key Challenges & Limitations
- **New Drivers Lack Historical Data** – Rookies or returnees (e.g., a 2025 mid-season replacement) won’t have prior F1 lap times, creating uncertainty.
- **Model Error (MAE: 3.47 sec)** – While useful for trends, real races are often decided by tenths of a second.
- **Race-Day Variables Not Included** – Tire degradation, pit strategy, and weather fluctuations significantly impact results but are not in this version.

---

## 🔮 Future Improvements
To enhance accuracy, future iterations could include:

- **Tire Strategy** – Soft tires degrade faster but offer initial speed, while hard tires last longer.
- **Weather & Track Conditions** – Rain can completely alter race outcomes, and grip levels change across a Grand Prix.
- **Race Pace Trends** – Some cars improve over long stints, while others drop off.
- **Pit-Stop Strategy** – Undercuts, overcuts, and safety cars often decide race positions.
- **Track-Specific Overtaking Difficulty** – A pass at Monza isn’t the same as one at Monaco.

---

## 🛠️ How to Use This Repository
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/navya-singhal/formula-1-race-prediction.git
cd formula-1-race-prediction
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
(If the `requirements.txt` file is missing, let me know—I can generate one.)

### 3️⃣ Run the Notebook
**For Jupyter Notebook:**
```bash
jupyter notebook
```
Open `Formula_1_2025_Prediction.ipynb` and run the cells.

**For Google Colab:**
Upload the notebook and execute the cells directly.

### 4️⃣ Experiment & Modify
- Adjust model parameters in `Formula_1_2025_Prediction.ipynb`.
- Add new features like weather conditions, tire degradation, or pit strategy.
- Try different ML models (Random Forest, XGBoost, etc.) for comparison.

### 5️⃣ Contribute
- Found an issue? Open a Pull Request or raise an Issue in the repo!
- Suggestions for improving the model? Let’s collaborate!

---

## 🏎️ Acknowledgments
- A special shoutout to **Mariana Antaya** for the inspiration behind this project! Check out her brief explaination on this ML prediction here: https://www.instagram.com/reel/DHP0otKuNly/?utm_source=ig_web_copy_link&igsh=MzRlODBiNWFlZA==

- This model is a work in progress, and as the **2025 F1 season unfolds**, I’ll continue refining it. Let’s see how well it holds up against real-world race results! 🚀

