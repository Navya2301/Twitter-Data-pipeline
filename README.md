# Twitter-Data-pipeline
This is End-To-End Data Engineering Project using Airflow and Python. In this project, we will extract data using Twitter API, use python to transform data, deploy the code on Airflow/EC2 and save the final result on Amazon S3

## Getting Started
1. Install python in your local machine
2. An AWS account
3. Install pandas, tweepy, s3fs
4. Use Twitter API to get the data, if you don't have v2 access get twitter data from Kaggle(https://www.kaggle.com/datasets/mmmarchetti/tweets-dataset)

## Steps
1. Login to AWS, to create an EC2 instance. Then diploy Airflow onto that. To do that once you create EC2 instance SSH into that and run .sh commands. It will install airflow and once it is installed then start the airflow server using following command
``` 
airflow standalone
```
2. Once the server is ready, you would be able to see the username and password. Now using the DNS in EC2 login to the website with the username and password provided.
3. To save the data onto a data frame we need to have S3 bucket so create one in AWS account. Also create an IAM role for EC2 instance to be able to access S3.
4. Login to airflow and create dag file. Run the server again to apply changes and then you will be able to see dag in the airflow UI. 
5. Once you run that you will be able to see the extracted data in S3
