pipeline {
    agent any
    tools{
        jdk 'Java-11'
        maven 'Maven'
    }
    stages{
        stage('git checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/ManojKRISHNAPPA/test-1.git'
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