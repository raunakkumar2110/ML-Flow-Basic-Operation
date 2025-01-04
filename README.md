# ML-Flow-Basic-Operation

## For Dagshub:

MLFLOW_TRACKING_URI= https://dagshub.com/raunakkumar2110/ML-Flow-Basic-Operation.mlflow \ 
MLFLOW_TRACKING_USERNAME=raunakkumar2110 \
MLFLOW_TRACKING_PASSWORD=bea1ab33dc7530c51e50ecbcbaa3ef64486c73fe \
python script.py



```bash

$env:MLFLOW_TRACKING_URI=https://dagshub.com/raunakkumar2110/ML-Flow-Basic-Operation.mlflow

$env:MLFLOW_TRACKING_USERNAME = "raunakkumar2110"
$env:MLFLOW_TRACKING_PASSWORD = "bea1ab33dc7530c51e50ecbcbaa3ef64486c73fe"



```
# MLflow on AWS

## MLflow on AWS Setup:

1. Login to AWS console.
2. Create IAM user with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv    //////     sudo apt install pipenv

sudo pip3 install virtualenv   //////      sudo apt install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-buc25
#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
$env:MLFLOW_TRACKING_URI = "http://ec2-52-23-185-41.compute-1.amazonaws.com:5000/"

```
