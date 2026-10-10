
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code is available in the workspace'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Run Java Program') {
            steps {
                bat 'java -cp target\\jenkins-maven-demo-1.0-SNAPSHOT.jar com.example.App'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESS!'
        }
        failure {
            echo 'BUILD FAILED. Check the Console Output.'
        }
    }
}
