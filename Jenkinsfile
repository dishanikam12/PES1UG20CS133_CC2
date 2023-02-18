pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS133 PES1UG20CS136.cpp'
                build job: 'PES1UG20CS136-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS136'
                
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
