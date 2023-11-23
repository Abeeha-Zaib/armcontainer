pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build the Docker image
                    sh 'docker build -t mypythonimage .'
                }
            }
        },
        stage('Run Python Script') {
            steps {
                script {
                    // Run commands inside the ARM64 container with Python installed
                    sh 'docker run --platform=linux/arm64/v8 mypythonimage /bin/bash -c "python3 setup_arm64.py build_ext --inplace -I ~/Python-aarch64-linux-gnu/_install3/include/python3.6/"'
                }
            }
        }
    }
}
