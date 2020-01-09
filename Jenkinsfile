pipeline {
    agent any

    stages {
        stage('Plan') {
            steps {
                sh 'terraform plan'
            }
        }
        stage('Initialize') {
            steps {
                sh 'terraform init'
            }
        }
        stage('Apply') {
            steps {
                sh 'terraform apply'
            }
        }
    }
}
