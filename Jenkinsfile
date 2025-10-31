// Jenkinsfile
pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Ravikiranmasule/jenkins_docker_java_hello_world.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('java-hello')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('java-hello').run()
                }
            }
        }
    }
}
