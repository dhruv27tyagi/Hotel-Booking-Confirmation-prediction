pipeline(
    agent any

    stages {
        stage('Cloning Github repo to Jenkins'){
            steps{
                script{
                    echo 'cloning github from jenkins.........'
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/dhruv27tyagi/Hotel-Booking-Confirmation-prediction.git']])
                }
            }
        }
    }
)