# Stock Price Prediction App

A full-stack web application for stock price prediction using machine learning. The backend is built with Flask and Python, featuring a Keras model for predictions, while the frontend is a modern React application built with Vite and TypeScript.

## Features

- Stock search functionality
- Real-time stock price prediction using a trained machine learning model
- Interactive charts displaying recent stock history
- Responsive UI with modern design components

## Prerequisites

Before running this application, ensure you have the following installed:

- **Python 3.8 or higher** (for the backend)
- **Node.js 16 or higher** (for the frontend)
- **npm** or **yarn** (package manager for Node.js)

## Installation

### Backend Setup

1. Navigate to the backend directory:
   ```
   cd "Stock Market Analysis/Backend"
   ```

2. Install Python dependencies:
   ```
   pip install -r requirements.txt
   ```

   This will install:
   - Flask
   - NumPy
   - Pandas
   - yfinance
   - scikit-learn
   - TensorFlow (for Keras)

### Frontend Setup

1. Navigate to the frontend directory:
   ```
   cd "Stock Market Analysis/frontend"
   ```

2. Install Node.js dependencies:
   ```
   npm install
   ```

   This will install all the required packages including React, Vite, TypeScript, and UI components.

## Running the Application

### Start the Backend

1. Ensure you're in the backend directory:
   ```
   cd "Stock Market Analysis/Backend"
   ```

2. Run the Flask application:
   ```
   python app.py
   ```

   The backend will start on `http://localhost:5000`.

### Start the Frontend

1. Open a new terminal and navigate to the frontend directory:
   ```
   cd "Stock Market Analysis/frontend"
   ```

2. Start the development server:
   ```
   npm run dev
   ```

   The frontend will start on `http://localhost:8080` (default Vite port).

## Usage

1. Open your browser and go to `http://localhost:8080`.
2. Use the search functionality to find stocks by ticker symbol or company name.
3. Select a stock to view its recent price history and get a prediction for the next day's closing price.
4. The prediction is generated using a trained Keras model based on the last 100 days of historical data.

## Project Structure

```
Stock Market Analysis/
├── Backend/
│   ├── app.py                 # Flask application
│   ├── requirements.txt       # Python dependencies
│   ├── Latest_stock_price_model.keras  # Trained ML model
│   └── stock_price.ipynb      # Jupyter notebook 
└── frontend/
    ├── src/
    │   ├── components/        # React components
    │   ├── pages/             # Page components
    │   └── lib/               # Utilities
    ├── package.json           # Node.js dependencies
    └── vite.config.ts         # Vite configuration
```

## Notes

- The machine learning model (`Latest_stock_price_model.keras`) must be present in the Backend directory for predictions to work.
- The application fetches real-time stock data using the yfinance library.
- CORS is enabled on the backend to allow communication with the frontend.
- For production deployment, consider using a proper web server like Gunicorn for Flask and building the frontend with `npm run build`.

## Troubleshooting

- If you encounter issues with the model loading, ensure TensorFlow/Keras is properly installed.
- For CORS errors, make sure the backend is running and accessible.
- If stock data cannot be fetched, check your internet connection and the validity of the ticker symbol.

## License

This project is for educational purposes. Please check the licenses of the individual libraries used.