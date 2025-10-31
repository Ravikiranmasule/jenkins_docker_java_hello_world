// Jenkinsfile
pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
              git branch: 'main', url: 'https://github.com/Ravikiranmasule/jenkins_docker_java_hello_world.git'

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
                   def output = sh(script: "docker run --rm java-hello", returnStdout: true).trim()
            echo "Java Output:\n${output}"
                }
            }
        }
    }
}
