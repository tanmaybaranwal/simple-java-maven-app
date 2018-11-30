pipeline {
    agent any
    tools {
        maven 'Maven 3.3.9'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage ('Clean') {
            steps {
                sh 'mvn clean package' 
            }
            post {
                success {
                    sh 'echo Package cleaned Hurrah' 
                }
            }
        }
    }
}
