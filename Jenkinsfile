pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps{
                 git 'https://github.com/Agr828/test/tree/master/src/com/demo'
            }
        }
        stage('Compile') {
            steps{
                 bat 'javac CalculatorDemo.java'
            }
        }
    }
    post {
        failure {
            mail bcc: '', body: "$BUILD_NUMBER", subject: "$JOB_NAME", to: 'yvsss81@@gmail.com'
        }
        success {
            mail bcc: '', body: "$BUILD_NUMBER", subject: "$JOB_NAME", to: 'yvsss81@gmail.com'
        }      
    }
}