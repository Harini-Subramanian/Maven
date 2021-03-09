pipeline {
    agent any
    stages {
        stage('Compile') {
            steps{
                bat 'echo Hello!'
            }
        }
    }
    post {
        failure {
            mail bcc: '', body: "$BUILD_NUMBER failure", subject: "$JOB_NAME", to: 'aharini545@gmail.com'
        }
        success {
            mail bcc: '', body: "$BUILD_NUMBER success", subject: "$JOB_NAME", to: 'aharini545@gmail.com'
        }      
    }
}
