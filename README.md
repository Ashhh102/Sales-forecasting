# Sales-forecasting
The project, "Temporal-Aware Sales Forecasting for Individual Products using Multi-Layer LSTM Networks," is an end-to-end time series forecasting solution designed to predict future product sales. It leverages deep learning techniques, particularly Bidirectional Long Short-Term Memory (BiLSTM) layers with an Attention mechanism, to capture complex temporal dependencies and enhance prediction accuracy for each product over time. The system is capable of handling large-scale retail data, capturing seasonality, trends, and sudden fluctuations in demand.

The model is trained on historical sales data and engineered features such as lag variables, rolling means, and time-related indicators (month, day, holidays). The preprocessing pipeline includes data normalization, missing value handling, and reshaping into a 3D format suitable for RNN input. Attention layers are applied on top of BiLSTM outputs to help the model focus on the most relevant time steps.

Key components of the project include:

Data Ingestion and Preprocessing: Handled via Pandas and NumPy, including temporal feature engineering and normalization.

Model Architecture: Constructed using Keras with a TensorFlow backend. It includes stacked BiLSTM layers followed by an Attention layer and Dense layers for prediction.

Training Configuration: The model is trained using the Adam optimizer with Mean Squared Error (MSE) loss. A learning rate scheduler and early stopping (patience=10) are applied to prevent overfitting.

Evaluation: The system uses Root Mean Squared Error (RMSE) and Mean Absolute Error (MAE) as primary evaluation metrics to assess forecast accuracy.

Deployment and Inference: Supports batch forecasting over test sets, and outputs are visualized using Matplotlib to compare predictions against ground truth.

The tool is optimized for both CPU and GPU execution and supports experimentation within Google Colab for ease of use. All dependencies are listed in the requirements.txt, and the codebase is modular for easy customization and extension. The system is practical for use by data scientists and retail analysts aiming to improve inventory planning and demand estimation.

