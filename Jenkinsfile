pipeline {
    agent any
    environment{
    APP_PORT = '9090'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building the app on port ${APP_PORT}"
                sh 'mvn -B package -DskipTests'
            }
        }
        stage('Unit Test') {
            steps {
                 echo 'Running unit tests'
                 sh 'mvn -B test'
            }
        }
    }
}
