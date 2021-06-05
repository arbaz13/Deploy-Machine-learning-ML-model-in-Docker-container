# Deploy-Machine-learning-ML-model-in-Docker-container



Task Description
1. Pull the Docker image of CentOS image from DockerHub and create a new container

2. Install the Python software on the top of docker container

3. Inside the Container you need to copy/create machine learning model and train it.


https://www.linkedin.com/pulse/deploy-machine-learningml-model-docker-container-arbaz-khan/?trackingId=nQzf%2BgNo%2FQXVCOy4akJKbA%3D%3D



Step 1: Install Docker

#yum install docker-ce --nobest -y

If You have already installed check for query

#rpm -q docker-ce



Step 2: Start Docker and Check Status

#systemctl start docker

#systemctl status docker



Step 3: Download the latest centos image from docker hub

#docker pull centos:latest


Step 4:Deploy a latest centos Container

#docker run -t -i --name myOs centos:latest


Step 5: Install Python 3 On Centos Container

#yum install python3


Step 6: Now install all the Required Packages

Numpy

Sklearn

Pandas

#pip3 install numpy && pip3 install sklearn && pip3 install pandas


Step 7: Copy dataset from base OS to Centos Container

#docker cp /root/SalaryData.csv myOs:/ML

Note: This command needs to be executed in your root where the data file in my case SalaryData.csv is stored



Step 8:Code to run ML model

model is provided in model.py file


Step 9: Run the Model

#python3 model.py


Thanks for reading :)

