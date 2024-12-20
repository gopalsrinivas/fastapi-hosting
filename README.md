Getting Started
Prerequisites
We assume that you have a amazon ec2 instance. In this tutorial we have used ubuntu with aws free tier and instance type is t2.micro(1 gb ram).

## After you enter the instance by ssh or any other method update the instance first by using below command:

sudo apt-get update

## Command to install python :

sudo apt install python3-pip

## Command to install git to clone this repository :

sudo apt install git

## Command to install git to clone this repository you can use your repository git url which you want to host :

sudo git clone Command to install git to clone this repository you can use your repository git url which you want to host :

sudo git clone https://github.com/gopalsrinivas/fastapi-hosting.git

ls -l

## Command to change location into the cloned folder you can use your repository name :

cd fastapi-hosting

## Command to install all the requirements required for the project to run in our case we have created requirements.txt file you can also create your own requirements :

pip install -r requirements.txt

## Command to run the API :

python3 -m uvicorn main:app --host 0.0.0.0 --port 8000
