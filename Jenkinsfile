pipeline {
    agent { docker { image 'gradle:6.7.1' } }
    stages {
        stage('build') {
            steps {
                sh 'gradle --version'
            }
        }
    }
}
