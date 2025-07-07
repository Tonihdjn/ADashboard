# Adashboard by Group 15

This is a dashboard web application designed to analyze sales data and perform customer segmentation using machine learning models. It is built using Python and Streamlit, with integration of the Darts library for time series forecasting and clustering models for customer segmentation.

## Project Structure

- **main.py**: The entry point for the Streamlit application. It handles the page configuration, data loading, and user interactions. It also visualizes the data using various charts and graphs.
  
- **prepro.py**: Contains functions for data preprocessing, including cleaning data, fixing column names, and preparing various aggregations for the dashboard (sales, customer data, etc.).

- **voice.py**: Provides text-to-speech and speech-to-text functionalities. This is used to interact with the dashboard through voice commands.

- **forecasting_model20.pth**: A saved forecasting model used for predicting future sales data (7 days ahead).

- **scaler.save**: A saved scaler used to scale the data before making predictions with the forecasting model.

- **Segmentasi_pembeli1.pkl** and **Segmentasi_pembeli22.pkl**: Saved customer segmentation models used for clustering customers based on their spending patterns.

## Installation

1. Clone this repository:

    ```bash
    git clone <repository-url>
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## How to Use

1. Run the Streamlit app:

    ```bash
    streamlit run main.py
    ```

2. On the homepage, upload a CSV file with the following columns:

    - Tanggal & Waktu
    - ID Struk
    - Tipe Penjualan
    - Nama Pelanggan
    - Nama Produk
    - Kategori
    - Jumlah Produk
    - Harga Produk
    - Metode Pembayaran

3. After the file is uploaded, the data will be cleaned and standardized. Then, you will be able to view various sales and customer data visualizations. You can also use the integrated chatbot to interact with the data using voice or text.

## Features

- **Sales Analysis**: View average daily sales, total products sold, and other key metrics.
- **Product Insights**: See the most sold products and analyze sales over time.
- **Customer Segmentation**: Segment customers based on spending habits using KMeans and DBSCAN clustering models.
- **Time Series Forecasting**: Forecast future sales using a pre-trained N-BEATS model.
- **Voice Interaction**: Use voice commands to interact with the dashboard, ask questions, or get data insights.

## Notes

- The app uses the `pytorch_forecasting` and `darts` libraries for time series forecasting and scaling.
- Models for customer segmentation and forecasting are pre-trained and saved as `.pkl` and `.pth` files.


