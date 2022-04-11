# CAN_Backend_logger Guide

## PRECURSOR:
Run each of these lines in the AWS EC2 Server in to uplaod to your respective S3 server. it shouldbe noted that this lines of code are specific to our
application of this implementation

IMPORTANT INFO FOR SETUP

Username:AndrewA200112

PERMAKEY:[KEY] Ask Andrew abrego or Chris gardner

## LOG INTO THE DASHBOARD
EMAIL: ProteusDataViewer@gmail.com
PASSWORD: Amazon123??

URL: https://aabrego2001.grafana.net/goto/wEbRMoUnz?orgId=1

It may take refreshing the page a couple of times in order to display the data properly

## Code for EC2 Server

Example lines that worked for application: 

THE FIRST TWO LINES WILL WORK CONSISTENTLY AND MUST BE UPLOADED 
followig this make keep cd'ing into directories until you you get to the canedge-grafan-backend

sudo apt update && sudo apt install python3 python3-pip python3-venv tmux python-is-python3 -y
git clone https://github.com/AndrewA200112/CAN_Backend_logger.git && cd CAN_Backend_logger && cd canedge-grafana-backend-main
python -m venv env && source env/bin/activate && pip install -r requirements.txt
tmux
python canedge_datasource_cli.py http://s3.us-east-1.amazonaws.com --port 8080 --limit 100 --s3_ak [KEY]--s3_sk [SECRET KEY] --s3_bucket battery-data-can 

^^For Key ASK Andrew Abrego or Chris Gardner for Key
