# AWS-Sagemaker-Project
In this project, I initiated the setup of an S3 bucket named 'bankpplication' within the 'us-east-2' region. To ensure compatibility with the specific region, I employed conditional statements, creating the bucket with a specified configuration. I handled potential errors, such as the bucket already being owned, to ensure a smooth creation process.

Subsequently, I facilitated the download of the dataset 'bank_clean.csv' from a provided URL using the urllib library. This step aimed to ensure the successful acquisition of the dataset. Following the download, I loaded the data into a Pandas dataframe, allowing for convenient manipulation and analysis.

To prepare for model training and evaluation, I conducted a train-test split on the dataset. The resulting training data comprised 28,831 samples, while the test data consisted of 12,357 samples. This division laid the groundwork for subsequent model development and assessment.

To streamline accessibility during the model training process, I saved both the training and test datasets into S3 buckets, naming them 'train' and 'test,' respectively. This approach facilitates organized data storage and retrieval during the model training phase.

For model development, I employed SageMaker's XGBoost built-in algorithm. I specified hyperparameters, including max depth, learning rate, and the objective function, to tailor the model's behavior. Following the training, I deployed the XGBoost model as an endpoint, making it available for real-time predictions and seamless integration into applications.

Using the deployed model, I conducted predictions on the test data, achieving an overall classification rate of 89.7%. This performance metric provides insights into the model's accuracy and effectiveness in making predictions.

Finally, to maintain a clean and efficient environment, I successfully deleted the SageMaker endpoint, ensuring the proper release of resources. Additionally, I cleared the S3 bucket, promoting data integrity and efficient utilization of cloud storage.
