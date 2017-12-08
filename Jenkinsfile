#!/usr/bin/env groovy
properties([
    [$class: 'GithubProjectProperty',
    displayName: '',
    projectUrlStr: 'http://52.207.55.50:8080'],
    pipelineTriggers([githubPush()])])

pipeline {
    agent {
        label{
            label 'Slavenode'
        }
    }
             parameters {
                            string(defaultValue: "default", description: 'Select Branch here ', name: 'Branch')
                           // choices are newline separated
                            choice(choices: 'Integration\nUnit', description: 'Used for posgress sh and codedeploy deployment group', name: 'Environment')
                            booleanParam(name: 'REBUILD DATABASE', defaultValue: true, description: 'Should we rebuild the database')
                            booleanParam(name: 'DEPLOY', defaultValue: true, description: 'should we deploy the application')
             }
    stages {
        stage('Build') { 
            steps { 
                echo 'Hello'
            }
        }
      
    }
}
