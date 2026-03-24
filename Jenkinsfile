pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/kavimani-sam/demo_deveops.git'
            }
        }

        stage('Install') {
            steps {
                dir('devops-ai-agents') {
                    bat 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                dir('devops-ai-agents') {
                    bat 'npm run build'
                }
            }
        }

        stage('Run') {
            steps {
                dir('devops-ai-agents') {
                    bat 'npm start'
                }
            }
        }
    }
}
