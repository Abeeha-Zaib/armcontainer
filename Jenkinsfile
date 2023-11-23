pipeline {
    agent any

    stages {
        stage('Update, Upgrade, and Install Python3') {
            steps {
                script {
                    // Run update, upgrade, and install Python 3 commands within the ARM64 container
                    sh 'docker run --platform=linux/arm64/v8 --rm ubuntu:latest /bin/bash -c "apt update && apt upgrade -y && apt install -y python3"'
                }
            }
        }
    }
}
