
pipeline {
    agent any

    stages {
        stage('Check Java Version') {
            steps {
                bat 'where java'
                bat 'java -version'
                bat 'where javac'
                bat 'javac -version'
                bat 'mvn -version'
            }
        }
    }
}
