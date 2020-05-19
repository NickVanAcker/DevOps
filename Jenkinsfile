pipeline {
    agent any
    
    stages {
        stage('Ok') {
            steps {
                echo "hello world"
            }
        }
    }
    post {
        always {
            emailext body: '${DEFAULT_CONTENT}',
                recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']],
                subject: '${DEFAULT_SUBJECT}'
        }
    }
}
