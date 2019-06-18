pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('test'){
            steps{
                sh './gradlew test'
            }
            post {
                always {
                    junit 'target/reports/*.xml' 
                }
            }
        }
    }
    post{
        success{
            echo 'Build Came Successfully'
        }
    }
}
