# IBM Back-end Capstone Songs Microservice

This is the Songs microservice created in Flask for main Capstone application. This microservice works with MongoDB database to store lyrics of the most popular songs of the band.

## Description

- Developed using Python and Flask following TDD.
- Install MongoDB on OpenShift.
- Use PyMongo to interact with MongoDB.
- Implement the service to retrieve song lyrics from the database.
- Create health endpoint for the microservice.
- Deployed to RedHat OpenShift.
- pytest for unit tests.

## Installation

Use the script to install virtual environment.
'''bash
cd /Back-End-Development-Songs
bash ./bin/setup.sh
'''

## Usage
'''bash
MONGODB_SERVICE=localhost MONGODB_USERNAME=root MONGODB_PASSWORD=password flask run --reload --debugger

curl -X GET -i -w '\n' localhost:5000/health
'''
