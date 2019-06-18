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
        }
        stage('Deliver') { 
            steps {
                sh './jenkins/scripts/deliver.sh' 
            }
        }
    }
    post{
        success{
            echo 'Build Came Successfully'
        }
    }
}
