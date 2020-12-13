// Uses Declarative syntax to run commands inside a container.
pipeline {
    agent {
        kubernetes {
            yamlFile 'jenkins-pod.yaml'
        }
    }
    stages {
        stage('Build') {
            steps {
                container('gradle') {
                    sh 'pwd'
                    sh 'ls -alh'
                    sh 'gradle build --no-daemon'
                    sh 'ls -alh'
                }
            }
        }
    }
}
