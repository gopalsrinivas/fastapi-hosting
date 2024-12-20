Getting Started
Prerequisites
We assume that you have a amazon ec2 instance. In this tutorial we have used ubuntu with aws free tier and instance type is t2.micro(1 gb ram).

## After you enter the instance by ssh or any other method update the instance first by using below command:

sudo apt-get update

## Command to install python :

sudo apt install python3 python3-pip python3-venv

## Command to install git to clone this repository :

sudo apt install git

## Command to install git to clone this repository you can use your repository git url which you want to host :

sudo git clone Command to install git to clone this repository you can use your repository git url which you want to host :

sudo git clone https://github.com/gopalsrinivas/fastapi-hosting.git

ls -l

## Command to change location into the cloned folder you can use your repository name :

cd fastapi-hosting

cd backend
sudo python3 -m venv myenv

source myenv/bin/activate

## Command to install all the requirements required for the project to run in our case we have created requirements.txt file you can also create your own requirements :

sudo chown -R ubuntu:ubuntu /home/ubuntu/fastapi-hosting/backend/myenv
sudo chmod -R u+rw /home/ubuntu/fastapi-hosting/backend/myenv

pip install -r requirements.txt

## Command to run the API :

python3 -m uvicorn app.main:app --host 0.0.0.0 --port 8000

## sample url:

http://43.204.141.42:8000/

## Development:

docker-compose up --build fastapi-dev

## Production

docker-compose up --build fastapi-prod

## Remove the containers with a single command (stop + remove)

docker stop fastapi_hostel_dev_container && docker rm fastapi_hostel_dev_container

docker stop fastapi_hostel_prod_container && docker rm fastapi_hostel_prod_container

## Removed

docker-compose build --no-cache fastapi-dev

## Access PostgreSQL Container:

docker exec -it postgres psql -U postgres -d fastapi_db
