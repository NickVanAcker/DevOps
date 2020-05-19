pipeline {
    agent any
     
    stages {
        stage('Ok') {
            steps {
                echo "Ok"
            }
        }
    }
    post {
        always {
            mail bcc: '', body: "<b>Example</b><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL de build: ${env.BUILD_URL}", cc: '', charset: 'UTF-8', from: 'jenkinsdevopsproject@gmail.com', mimeType: 'text/html', replyTo: '', subject: "BUILD CI: Project name -> ${env.JOB_NAME}", to: "thenoob551@gmail.com";
        }
    }
}
