
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code checked out from GitHub'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Run Java Program') {
            steps {
                bat '"C:\\Program Files\\java\\jdk-21.0.12.1\\bin\\java.exe" -cp target\\jenkins-maven-demo-1.0-SNAPSHOT.jar com.example.App'
            }
        }
    }

    post {
        success {
            echo 'Build and execution successful!'
        }
        failure {
            echo 'Build or execution failed!'
        }
    }
}
