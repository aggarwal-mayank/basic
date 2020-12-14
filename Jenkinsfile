// Uses Declarative syntax to run commands inside a container.
pipeline {
    agent {
        kubernetes {
            yamlFile 'jenkins-pod.yaml'
        }
    }
    stages {
        stage('Test') {
            steps {
                container('gradle') {
                    sh 'pwd'
                    sh 'gradle test'
                    sh 'ls -alh'
                }
            }
        }

        stage('Build') {
            steps {
                container('gradle') {
                    sh 'pwd'
                    sh 'gradle fatJar'
                    sh 'ls -alh'
                }
            }
        }
    }
}
