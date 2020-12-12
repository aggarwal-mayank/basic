pipeline {
     agent kubernetes
     triggers {
        pollSCM '2 * * * *'
     }
         environment {
             // Using returnStdout
             CC = """${sh(
                     returnStdout: true,
                     script: 'echo "clang"'
                 )}"""
             // Using returnStatus
             EXIT_STATUS = """${sh(
                     returnStatus: true,
                     script: 'exit 1'
                 )}"""
         }
     stages {
        stage('Build') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage('Test') {
            environment {
                DEBUG_FLAGS = '-g'
            }
            steps {
                sh 'printenv'
            }
        }
        stage('Deploy') {
            steps {
                sleep(time:1,unit:"MINUTES")
            }
        }
    }
}
