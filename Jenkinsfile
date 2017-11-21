pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                echo 'sh not working..'
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