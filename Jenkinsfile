pipeline {
    agent any

    tools {
        jdk 'jdk11'          // Configure in Jenkins (Global Tool Config)
        maven 'maven3'       // Optional (if using Maven)
    }

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/kavimani-sam/demo_deveops.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo Deploy step here'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
