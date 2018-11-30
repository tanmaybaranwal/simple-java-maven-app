pipeline {
    agent any
    tools {
        maven 'Maven'
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
