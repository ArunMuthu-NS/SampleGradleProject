pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
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
