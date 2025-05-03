pipeline {
    agent any

    stages {
        stage('Compilar') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Pruebas') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            junit 'target/surefire-reports/*.xml'
        }
    }
}
