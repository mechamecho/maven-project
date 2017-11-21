pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'echo hello there'
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