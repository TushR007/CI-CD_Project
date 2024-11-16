pipeline {
    agent any
    tools{
        jdk 'java-11'
        maven 'maven'
    }
    stages{
        stage('git checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/TushR007/CI-CD_Project.git'
            }
        }
        stage('compile'){
            steps{
                sh "mvn compile"
            }
        }
        stage('Build'){
            steps{
                sh "mvn clean install" 
            }
        }

    }
}