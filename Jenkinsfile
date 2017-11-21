pipeline {
    agent any
    stages{
        stage('Build'){
            def mvn_version = 'M3'
            withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] )
            steps {
                sh 'mvn clean package'
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