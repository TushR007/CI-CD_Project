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
                sh "mvn package" 
            }
        }
        stage('Build and Tag Dockerfile'){
            steps{
                sh 'Build -t TushR007/CIProj:1 .'
            }
        }
        stage('Containerisation'){
            steps{
                sh 'docker run -it -d --name c1 8081:8080 TushR007/CI-CD_Project:1'
            }
        }
    }
}