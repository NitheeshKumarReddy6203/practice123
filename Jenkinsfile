pipeline {
    agent any

    stages {
        stage('CheckOut') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '6203', url: 'https://github.com/NitheeshKumarReddy6203/practice123.git']])
                echo "\nCheckout is Completed\n\n"
            }
        }
        stage('Run Python Script') {
            steps {
                sh "python3 print.py"
            }
        }
        stage('CheckOut in feature-dev Branch!') {
            steps {
                checkout scmGit(branches: [[name: '*/feature-dev']], extensions: [], userRemoteConfigs: [[credentialsId: '6203', url: 'https://github.com/NitheeshKumarReddy6203/practice123.git']])
                echo "\nCheckout is Completed\n\n"
            }
        }
        stage('Run Python Script in new Branch!') {
            steps {
                sh "python3 nums.py"
            }
        }
    }
}
