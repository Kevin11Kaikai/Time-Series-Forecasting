Time Series Forecasting with Deep Learning for Solar Panel Data
This project explores and compares the performance of four deep learning architectures—Recurrent Neural Networks (RNN), Long Short-Term Memory (LSTM), Gated Recurrent Units (GRU), and Transformers—for predicting two time-series signals, Ot and Rt, from solar panel data.

📝 Project Overview
The dataset consists of signals sampled every 15 minutes over 11 months. The primary objective is to develop, train, evaluate, and fine-tune these neural network models to identify the most effective architecture for this forecasting task. Model performance is benchmarked using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R²) metrics.

✨ Features
Four Powerful Models: Implementation and comparison of RNN, LSTM, GRU, and Transformer architectures.

Comprehensive Evaluation: Models are assessed using MSE, MAE, and R² to provide a holistic view of their performance.

Hyperparameter Tuning: An extensive tuning process is documented to find the optimal configuration for each model.

Detailed Analysis: The accompanying report and notebook provide in-depth analysis and discussion of the results.

📁 File Descriptions
ECE_2795_final_Yukai_Song_Report.pdf: The main project report providing a detailed analysis of the models, methodology, and results.

ECE_2795_final_Yukai_Song_Code.ipynb: A Jupyter Notebook containing all Python code for data preprocessing, model implementation, training, and evaluation.

timeseries_data_2024.csv: The raw dataset containing the time-series data for the Ot and Rt signals.

🚀 Getting Started
To get this project up and running on your local machine, follow these steps.

Prerequisites
You will need Python 3 and the following libraries installed:

pandas

numpy

tensorflow

scikit-learn

matplotlib

tabulate

Installation & Usage
Clone the repository (if applicable) and install dependencies:

pip install pandas numpy tensorflow scikit-learn matplotlib tabulate

Prepare the data: Place the timeseries_data_2024.csv file in the same directory as the ECE_2795_final_Yukai_Song_Code.ipynb notebook.

Run the analysis: Open the Jupyter Notebook and run the cells sequentially. The notebook is organized into the following sections:

Data Preparation: Loads and preprocesses the time-series data.

Model Implementation and Training: Defines, trains, and evaluates each of the four models.

Hyperparameter Tuning: Contains the code for fine-tuning the models to find the best-performing parameters.

Results and Comparison: Summarizes the performance of each model and provides a comparative analysis.

📊 Model Performance
The performance of each model was evaluated on the testing set for both the Ot and Rt signals.

Initial Model Performance
Model

Target

MSE

MAE

R²

RNN

Ot

0.0433

0.1434

0.3599



Rt

0.0089

0.0579

0.5829

LSTM

Ot

0.0442

0.1498

0.3464



Rt

0.0134

0.0713

0.3699

GRU

Ot

0.0433

0.1366

0.3599



Rt

0.0081

0.0565

0.6179

Transformer

Ot

0.0426

0.1495

0.3711



Rt

0.0079

0.0521

0.6293

🏆 Best Models After Hyperparameter Tuning
After an extensive hyperparameter tuning process, the best models were identified based on the lowest Mean Squared Error (MSE):

For the Ot signal: The best-performing model was an LSTM with an MSE of 0.0422.

Best parameters: 3 layers, 250 units, a learning rate of 1e-4, and a dropout rate of 0.3.

For the Rt signal: The best-performing model was also an LSTM with an MSE of 0.0076.

Best parameters: 3 layers, 250 units, a learning rate of 5e-5, and a dropout rate of 0.3.

💡 Conclusion
This project demonstrates the application of various neural network architectures for time-series forecasting. While the Transformer and GRU models showed strong initial performance, the LSTM model, after hyperparameter tuning, proved to be the most effective for both signals. This suggests that for this particular dataset, the gating mechanisms of LSTMs provide an optimal balance of complexity and efficiency in capturing temporal dependencies.

🧑‍💻 Author
This project was created by Yukai Song.
