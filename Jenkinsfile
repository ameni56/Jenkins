pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                // Checkout the Git repository
                git 'https://github.com/ameni56/Jenkins.git'
            }
        }

        stage('Maven Build') {
            steps {
                // Use Maven wrapper if available, or use a specific Maven installation
                sh './mvnw clean package || mvn clean package'
            }
        }

        stage('Maven Test') {
            steps {
                // Use Maven wrapper if available, or use a specific Maven installation
                sh './mvnw test || mvn test'
            }
        }
    }
}
