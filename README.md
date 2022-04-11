# CAN_Backend_logger Guide

## Precursor:
This application serves to provide insight on a useful data visualization tool to model Battery Data Logged Over the CAN data bus that includes power, voltage,current,,temperature, and individual cell readings. This Project was worked on by Andrew Abrego and Chris Garner at Amazon Robotics during Spring 2022

Run each of these lines in the AWS EC2 Server in to uplaod to your respective S3 server. it shouldbe noted that this lines of code are specific to our
application of this implementation

IMPORTANT INFO FOR SETUP

Username:AndrewA200112

PERMAKEY:[KEY] Ask Andrew abrego or Chris gardner

## Log Into Dashboard
Below are the login credientials to view the server from an external account. 
* Dashboard Link: https://aabrego2001.grafana.net/goto/wEbRMoUnz?orgId=1
* Email: ProteusDataViewer@gmail.com
* Password: Amazon123??


### Data not Displaying?
It may take refreshing the page a couple of times in order to display the data properly. Typically it may take around 4 refreshes for the data to be displayed on the dashboard. The refresh button can be found in the top right corner of the dashboard link.

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
