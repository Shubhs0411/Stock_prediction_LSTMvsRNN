# 📈 Stock Market Prediction using RNN vs LSTM

This project builds and compares **Recurrent Neural Network (RNN)** and **Long Short-Term Memory (LSTM)** models to forecast **Google stock prices** using historical data. It demonstrates the strengths and limitations of deep learning techniques in time series forecasting.

---

## 🧠 Objective

- Predict the **next-day stock price** based on past observations.
- Compare RNN and LSTM architectures in terms of performance and interpretability.
- Explore common challenges like overfitting, temporal dependencies, and lag effects.

---

## 🗃️ Dataset

- **Google_Stock_Price_Train.csv** and **Google_Stock_Price_Test.csv**
- Source: [Yahoo Finance](https://finance.yahoo.com/)
- Fields: `Open`, `High`, `Low`, `Close`, `Volume` (used `Open` price for prediction)

---

## ⚙️ Tech Stack

- **Language:** Python  
- **Libraries:** `Pandas`, `NumPy`, `Matplotlib`, `Scikit-learn`, `TensorFlow/Keras`
- **Models:** RNN, LSTM (Sequential Keras models)

---

## 🔄 Workflow

1. **Data Preprocessing**
   - Feature selection (`Open` price)
   - Normalization using `MinMaxScaler`
   - Windowed sequence generation (60-day lookback)

2. **Model Architecture**
   - RNN: 2 SimpleRNN layers + Dense output
   - LSTM: 2 LSTM layers + Dense output
   - Loss: Mean Squared Error  
   - Optimizer: Adam

3. **Evaluation**
   - Metrics: RMSE, MAE
   - Visualization of true vs predicted values
   - Insight on RNN vs LSTM generalization and lag handling

---

## 📊 Results

| Model  | RMSE     | MAE      |
|--------|----------|----------|
| RNN    | ~12.04   | ~9.87    |
| LSTM   | ~9.32    | ~7.45    |

- LSTM outperforms RNN on long-term dependencies.
- RNN tends to underfit due to vanishing gradients on longer sequences.

---

## 📌 Key Insights

- **LSTM captures longer trends** better due to memory gating.
- **Overfitting control** via dropout and early stopping was crucial.
- Showcases practical deep learning use in **finance** and **time series modeling**.

---

## 💡 Future Improvements

- Add GRU model for comparison.
- Use additional features (`High`, `Low`, `Volume`) for multivariate forecasting.
- Integrate external factors like sentiment or macroeconomic data.

---

## 🧑‍💻 Author

**Shubham Deshmukh**  
📧 shubhamd23@vt.edu  
🔗 [LinkedIn](https://www.linkedin.com/in/shubhdesh) | [Portfolio](https://shubhs0411.github.io/react-portfolio/) | [Resume](https://github.com/Shubhs0411)

---

## 📁 License

This project is licensed under the MIT License.
