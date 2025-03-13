# BTC Price Predictor	 

This project implements a Bitcoin price predictor using a Long Short-Term Memory (LSTM) neural network. The model is trained on historical Bitcoin prices obtained via the `yfinance` library, and it forecasts future prices based on past trends.

## Features

- Fetches Bitcoin historical data for the past five years using `yfinance`
- Preprocesses data using `MinMaxScaler` for better model convergence
- Implements an LSTM model with dropout layers to prevent overfitting
- Predicts future Bitcoin prices and visualizes actual vs. predicted prices

## Dependencies

Ensure the following Python libraries are installed:

```bash
pip install tensorflow pandas numpy matplotlib yfinance scikit-learn keras
```

## Model Architecture

The LSTM model is built using Keras with the following structure:

- 4 LSTM layers with 100, 100, 50, and 50 units respectively
- Dropout layers (0.2) after each LSTM layer
- Dense output layer to predict future Bitcoin price
- Optimizer: Adam
- Loss function: Mean Squared Error (MSE)

## How to Run the Project

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd bitcoin-predictor
   ```

2. Ensure you have the required packages:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the script:

   ```bash
   python bitcoin_predictor.py
   ```

## Outputs
- Line plot comparing actual Bitcoin prices with predicted prices

## Methodology

1. **Data Collection**: Fetches the last 5 years of Bitcoin data.
2. **Data Preprocessing**: Scales prices using MinMaxScaler and creates sequences for training.
3. **Model Training**: Trains an LSTM model for 50 epochs with a batch size of 32.
4. **Prediction**: Predicts future prices and compares them with actual values.
5. **Visualization**: Plots the real vs. predicted Bitcoin prices over time.

## References

- [TensorFlow Documentation](https://www.tensorflow.org/)
- [Keras Sequential Model](https://keras.io/guides/sequential_model/)
- [yFinance API](https://github.com/ranaroussi/yfinance)

## License

This project is licensed under the MIT License.


