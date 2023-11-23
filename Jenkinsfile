pipeline {
    agent any

    stages {
        stage('Pull and Run ARM64 Container') {
            steps {
                script {
                    // Run commands inside the ARM64 container
                    sh 'docker run --platform=linux/arm64/v8 ubuntu:latest /bin/bash -c "python3 setup_arm64.py build_ext --inplace -I ~/Python-aarch64-linux-gnu/_install3/include/python3.6/"'
                }
            }
        }
    }
}
