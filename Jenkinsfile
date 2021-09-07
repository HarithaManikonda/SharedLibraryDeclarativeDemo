#!groovy
@Library("shared-libraray") _
pipeline {
    agent any
    
    tools {
        maven 'maven'
        jdk 'jdk8'
    }
    

    stages {
    
    stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying through Shared library ....'
                script {
                 welcome.call("Haritha")
                    }
            }
        }
    }
    
    
}
