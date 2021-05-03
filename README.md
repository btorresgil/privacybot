# PrivacyBot

PrivacyBot is a simple automated service to initiate CCPA deletion requests with databrokers.

## How It Works
1. PrivacyBot comprises of a React Frontend and a Python Flask Backend web architecture
2. After starting the application, PrivacyBot initiates an OAuth authentication request with your Gmail account. You will be asked to allow PrivacyBot to read, compose and send emails from your Gmail account. 
3. Once the authentication is successfully completed, depending on the data provided to the Flask API, a CCPA data delete email is drafted and sent to the data brokers chosen. 
4. A confirmation email is sent listing all the databrokers to whom the email was sent or not sent. 

## Usage

### Prerequisites

1. A Gmail account - This is the email from which you will be initiating the data delete requests. PrivacyBot's data deletion process is most effective if this email is the one which you use the most for personal use. 
2. Python 3 (https://www.python.org/downloads/)
3. Ensure pip3 is installed (https://pip.pypa.io/en/stable/installing/)
4. Install node https://nodejs.org/en/download/ 

#### 1. Download zip file from Github Repo and unzip 

#### 2. Open Visual Studio Code and open the “privacybot-private-main” folder 

#### 3. Open split terminal in VS Code (or any two terminals/cmd prompts on your machine). We will be using one terminal to run the Flask app and the other one to run the React app.


## Start the Flask Server 

#### 1. Create and activate a Python Virtual Environment 

The below commands create and activate a virtual environment named "PB_venv". 

`$ python3 -m venv PB_venv` 

`$ source PB_venv/bin/activate`

#### 2. Install from requirements.txt

`$ pip3 install -r requirements.txt`

To confirm required packages are installed - see if “flask_cors” is installed:
`$ pip3 list`

#### 3: Start Flask App
Run the below commands within the activated virtual environment.

`$ cd app`

`$ flask run`

The above commands should start the flask application. It can now be accessed through http://127.0.0.1:5000/

Leave this terminal instance as is, and open the second terminal instance. 

## Start the React Application
PFB a step by step list of commands / guide that informs how to install an instance of the React Server. 

#### 1. Run the following commands in the second terminal: 

`$ cd PB_UI`

#### 2. Check to make sure node and npm is correctly installed

`$ node -v`

`$ npm-v`

#### 3. Install the required packages using npm install. Fix any vulnerabilities found. 
`$ npm install`

`$ npm audit fix`

#### 4. Start the React Application by running the below commands
`$ npm run build`

`$ npm start`

#### 5. Follow the steps and authenticate your Gmail account 

#### 6. Remove access to PrivacyBot from your Gmail account
