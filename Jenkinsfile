pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS133 PES1UG20CS133.cpp'
                build job: 'PES1UG20CS133-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS133'
                
            }
        }

        stage('Deploy') {
            steps {
               
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
