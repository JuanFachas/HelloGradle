pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Hello World') {
            steps {
                sh 'javac src/main/java/Main.java'
                sh 'java -cp src/main/java Main'
            }
        }
    }

    post {
        success {
            echo '✅ Hello World ejecutado desde Jenkins.'
        }
        failure {
            echo '❌ Falló la ejecución de Hello World.'
        }
    }
}
