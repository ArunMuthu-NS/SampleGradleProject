pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh './gradlew build'
            }
        }
    }
    post{
        success{
            echo 'Build Came Successfully'
        }
    }
}
