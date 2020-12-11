pipeline {
    agent { docker 'openjdk:11' } 
    stages {
        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }
    }
}
