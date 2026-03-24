pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/kavimani-sam/demo_deveops.git'
            }
        }

        stage('Install & Run') {
            steps {
                bat 'yarn install'
                bat 'yarn start'
            }
        }
    }
}
