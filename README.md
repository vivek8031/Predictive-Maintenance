# Predictive Maintenance

This repository contains a Jupyter notebook that guides you through the process of building a predictive maintenance model for turbofan engines using Amazon SageMaker.

The notebook makes use of a dataset provided by NASA's Prognostic Center of Excellence. This dataset is built upon a high fidelity simulation of a turbofan engine (C-MAPSS). Synthetic faults and continuous degradation trends have been injected into the dataset to simulate real-world scenarios. The dataset is publicly available and is widely used for benchmarking prognostics and predictive maintenance algorithms.

## Content

The Jupyter notebook is divided into several sections, each focusing on a different aspect of the data science process:

1. **Data Preparation**: This section provides a brief overview of the complexities of gathering, storing, and preparing real-world data for predictive maintenance tasks. It also introduces the C-MAPSS dataset used in the notebook.

2. **Process Data**: This part involves reading and preprocessing the training and test datasets. The preprocessing includes computation of the Remaining Useful Life (RUL) for each engine in the dataset and normalization of the sensor readings to a range between 0 and 1. This section also includes visualizations of several columns from the training data for better understanding.

3. **SageMaker MXNet Estimator**: This section provides a detailed explanation of how to define and train a MXNet model with Amazon SageMaker.

4. **Upload Processed Data to S3 for Training**: The processed training and test data are uploaded to an S3 bucket. This step is necessary because the SageMaker training instance accesses the data from this S3 location. The test data is also stored in the S3 bucket for later use in model evaluation.

5. **Set Model Output Location**: This section defines the location where the model output will be stored.

## Usage

To use this notebook:

1. Clone the repository to your local machine or cloud environment.
2. Make sure you have the necessary Python packages installed (see "Requirements" below).
3. Open the Jupyter notebook and follow the steps outlined in it.

## Requirements

To run this notebook, you'll need:

- Python 3.x
- Jupyter Notebook
- AWS SDK for Python (Boto3)
- Amazon SageMaker Python SDK
- MXNet

## Contribute

Please feel free to fork this repository, submit PRs, and raise issues.

## License

This project is licensed under the terms of the MIT license.
