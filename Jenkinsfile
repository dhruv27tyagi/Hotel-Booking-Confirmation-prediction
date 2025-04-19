pipeline{
    agent any

    environment {
        VENV_DIR = 'venv'
    }

    stages {
        stage('Cloning Github repo to Jenkins'){
            steps{
                script{
                    echo 'cloning github from jenkins.........'
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/dhruv27tyagi/Hotel-Booking-Confirmation-prediction.git']])
                }
            }
        }

        stage('Setting up our virtual environment and installing dependencies'){
            steps{
                script{
                    echo 'Setting up our virtual environment and installing dependencies'
                    sh '''
                    python -m venv ${VENV_DIR}
                    . ${VENV_DIR}/bin/activate
                    pip install --upgrade pip
                    pip install -e .
                    '''
                }
            }
        }
    }
}