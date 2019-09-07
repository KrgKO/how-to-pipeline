# How to running pipeline on jenkins

Try to learning pipeline on jenkins with pipeline on groovy

## Getting started

1. `docker-compose up -d` - To start docker-container of jenkins

Note: make sure that jenkins_home folder has been created correctly

2. Find secret and register at jenkins at `http://localhost:8077` from `/var/jenkins_home/secrets/initialAdminPassword`
3. Install plugins
4. Register admin

## Start pipeline

1. Install pipeline by go to `Manage jenkins > Manage plugin > Available` then search pipeline to install
2. Start to create pipeline
3. Create groovy script then save
```groovy
pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building ...'
            }
        }
        stage('Test') {
            steps {
                echo 'Test ...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy ...'
            }
        }
    }
}
```
4. Go to job console and click `build now` ... Check the result