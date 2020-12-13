// Uses Declarative syntax to run commands inside a container.
pipeline {
    agent {
        kubernetes {
            yamlFile 'jenkins-pod.yaml'
        }
    }
    stages {
        stage('Main') {
            steps {
                container('shell') {
                    sh 'pwd'
                    sh 'ls -alh'
                }
            }
        }
    }
}
