pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/prameervidhate/spring-boot.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                sh 'cp target/*.war /opt/tomcat/webapps/'  // Tomcat path ke according update karo
            }
        }
    }
}
