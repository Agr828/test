pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps{
                 git 'https://github.com/Agr828/test'
            }
        }//compile
        stage('Compile') {
            steps{
                 bat 'echo hello'
            }
        }
    }//te
    post {
        failure {
            mail bcc: '', body: "$BUILD_NUMBER", subject: "$JOB_NAME", to: 'yvsss81@gmail.com'
        }
        success {
            mail bcc: '', body: "$BUILD_NUMBER", subject: "$JOB_NAME", to: 'yvsss81@gmail.com'
        }      
    }
}