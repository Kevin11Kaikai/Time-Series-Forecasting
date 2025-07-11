# 🌞 Time Series Forecasting for Solar Panel Data

## 📌 Task
Forecast solar panel signals `Ot` & `Rt` (15‑minute intervals, 11 months) using:
- RNN
- LSTM
- GRU
- Transformer  

---

## 📊 Dataset
- **File**: `timeseries_data_2024.csv`  
- **Features**: `Ot`, `Rt`  
- **Preprocessing steps**:  
  1. 80% train / 20% test split  
  2. Sliding‑window sequence creation (length = 32)  
  3. `MinMaxScaler` normalization  

---

## ⚙️ Models Implemented

### 1. RNN
- Basic recurrent model  
- Easy to implement, but limited  

### 2. LSTM
- Captures long-term dependencies  
- Best performance after tuning  

### 3. GRU
- Simplified LSTM  
- Efficient with competitive accuracy  

### 4. Transformer
- Self-attention for global patterns  
- Excels on `Rt` forecasting  

---

## 🔧 Hyperparameter Tuning
| Parameter       | Candidates                   |
|----------------|------------------------------|
| Learning rate  | 1e-3 → 1e-4, 5e-5, 1e-5       |
| Hidden units   | 250, 350                     |
| Layers         | 2, 3                         |
| Dropout        | 0.3                          |
| Transformer    | d_model: 128/256, heads: 2/4, FF units: 2048/3072 |

---

## 📈 Evaluation Metrics
- **MSE**: Mean Squared Error  
- **MAE**: Mean Absolute Error  
- **R²**: Coefficient of Determination  

---

## 🏅 Results

### Raw Models
| Model       | Target | MSE     | MAE     | R²     |
|------------|--------|---------|---------|--------|
| RNN        | Ot     | 0.0433  | 0.1434  | 0.3599 |
| RNN        | Rt     | 0.0089  | 0.0579  | 0.5829 |
| LSTM       | Ot     | 0.0442  | 0.1498  | 0.3464 |
| LSTM       | Rt     | 0.0134  | 0.0713  | 0.3699 |
| GRU        | Ot     | 0.0433  | 0.1366  | 0.3599 |
| GRU        | Rt     | 0.0081  | 0.0565  | 0.6179 |
| Transformer| Ot     | 0.0426  | 0.1495  | 0.3711 |
| Transformer| Rt     | 0.0079  | 0.0521  | 0.6293 |

### Best Tuned Models
- **Ot**: LSTM (3 layers, units=250, lr=1e-4) → **MSE = 0.0422**  
- **Rt**: LSTM (3 layers, units=250, lr=5e-5) → **MSE = 0.0076**  

---

## 💡 Key Insights
- ✅ **LSTM** delivers best overall accuracy with tuning  
- ⚡ **Transformer** shows impressive performance on `Rt` without heavy tuning  
- 🤖 **GRU** is efficient and effective  
- ⚠️ **RNN** is simple but prone to vanishing gradients  

---

## 🗂️ Files Overview
- `timeseries_data_2024.csv` — dataset  
- `ECE_2795_final_Yukai_Song_Code.ipynb` — training & evaluation notebook  
- `ECE_2795_final_Yukai_Song_Report.pdf` — detailed report  

---

## 🚀 How to Run
```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Launch notebook
jupyter notebook ECE_2795_final_Yukai_Song_Code.ipynb
