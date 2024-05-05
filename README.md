# Data Generation Process

Follow the steps below to generate and process the data:

1. Execute all the code in `preprocess_SP500.ipynb`.
2. Run the `get_data()` function in `preprocessing_stock_price.ipynb` to download the related stock data. This needs to be done only once.
3. Execute the remaining code of `preprocess_stock_price.ipynb` until `extract_data()`. Adjust parameters to generate different datasets. Note that the latest `extract_data()` call will overlap the previous one.
4. Run `standardize`, `minmax_scaler` to get the corresponding scaler. Note that these are not applied in the final model.
5. Zip the `/data` directory and upload it to Google Drive.

# Model Training Process

Follow the steps below to train the model:

1. Upload `model_training_XX.ipynb` notebook to Colab, modify the zip file path to the correct location.
2. Adjust parameters to make them compatible with the data generator.
3. If needed, adjust the model parameters.
4. Train the model using `train.fit`.
5. Evaluate model performance with label accuracy and `backtest()`.
