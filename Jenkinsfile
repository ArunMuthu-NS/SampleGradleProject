pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                ./gradlew build
            }
        }
    }
    post{
        success{
            mail to: 'arunmuthu.ns@gmail.com',
             subject: "Success Pipeline: ${currentBuild.fullDisplayName}",
             body: "Successfully Deployed Build ${env.BUILD_URL}"
 
        }
    }
}
