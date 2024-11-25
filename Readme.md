# Crypto Price Analysis Web App

This is a Flask-based web application for analyzing cryptocurrency price trends. The app displays a candlestick chart along with technical indicators like Moving Averages, RSI (Relative Strength Index), Bollinger Bands, and MACD (Moving Average Convergence Divergence).

## Features

- **Interactive Candlestick Chart**:
  Visualize cryptocurrency price data with dynamic candlestick charts.

- **Technical Indicators**:
  Includes Moving Averages (30-day and 50-day), RSI, Bollinger Bands, and MACD for deeper analysis.

- **Date Range Filtering**:
  Users can specify the start and end date to visualize specific time periods.

- **Dark Mode**:
  Toggle between light and dark modes for better visual comfort.

- **Download Data**:
  Export the cryptocurrency data in CSV format.

## Technologies Used

- **Backend**:
  - Flask for server-side logic.
  - `yfinance` for fetching cryptocurrency data.
  
- **Frontend**:
  - Plotly for interactive chart rendering.
  - HTML and CSS for styling.

- **Libraries**:
  - `plotly` for graph rendering.
  - `pandas` for data manipulation.
  - `io` for data export functionality.

## Prerequisites

1. Python 3.8 or higher installed.
2. Install required Python libraries using:

   ```bash
   pip install -r requirements.txt
   ```

   Example `requirements.txt` file:

   ```
   Flask
   yfinance
   plotly
   pandas
   ```

## How to Run the Application

1. Clone the repository:

   ```bash
   git clone https://github.com/vermu490/crypto-dashboard
   cd crypto-dashboard
   ```

2. Start the Flask server:

   ```bash
   python bct.py
   ```

3. Open your browser and navigate to:

   ```
   http://127.0.0.1:5000
   ```

## How to Use

1. **Enter Cryptocurrency**:
   - Input the cryptocurrency symbol (e.g., `BTC-USD`, `ETH-USD`).

2. **Set Date Range**:
   - Specify the start and end dates for the analysis.

3. **View Charts**:
   - Analyze the interactive chart and various indicators.

4. **Download Data**:
   - Click the "Download Data as CSV" button to save the historical data.

5. **Toggle Themes**:
   - Use the "Switch to Dark Mode" button to change themes.

## API Reference

### Data Source
The app fetches historical cryptocurrency data using the `yfinance` API.

### Endpoints

- `/`:
  - Displays the main dashboard with the chart and indicators.
  
- `/download`:
  - Downloads the cryptocurrency data as a CSV file.

## Code Overview

### Main Files

1. **`bct.py`**:
   - Core application logic.
   - Fetches cryptocurrency data, computes indicators, and renders the template.

2. **Functions**:
   - `get_data()`: Fetches historical data using `yfinance`.
   - `compute_rsi()`: Computes RSI values.
   - `compute_bollinger_bands()`: Calculates Bollinger Bands.
   - `compute_macd()`: Derives MACD and its signal line.

3. **Template**:
   - Uses `render_template_string()` for the front-end.

### Indicators Explained

- **Moving Average (MA)**:
  - Averages the closing price over 30 or 50 days.

- **Relative Strength Index (RSI)**:
  - Evaluates overbought or oversold conditions.

- **Bollinger Bands**:
  - Indicates price volatility with upper and lower bands.

- **MACD**:
  - Shows momentum and potential trend reversals.

## Contributing

Feel free to submit issues or pull requests for any improvements or bug fixes.