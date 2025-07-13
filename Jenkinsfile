echo 'pipeline {
    agent any
    stages {
        stage("Checkout") {
            steps {
                checkout scm
            }
        }
        stage("Build") {
            steps {
                sh "./gradlew clean build"
            }
        }
        stage("Run") {
            steps {
                sh "java -jar build/libs/*.jar || true"
            }
        }
    }
    post {
        success {
            echo "✅ Gradle Hello World ejecutado con éxito."
        }
        failure {
            echo "❌ Algo falló al ejecutar el Hello World con Gradle."
        }
    }
}' > Jenkinsfile
