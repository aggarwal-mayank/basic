pipeline {
    agent any
    triggers {
  pollSCM '2 * * * *'
}
        stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sleep(time:5,unit:"MINUTES")
            }
        }
    }
}
