pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh "echo Hello World!"
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}