pipeline {
    agent {
  label 'jenkins-master'
}


    stages {
        stage('compile') {
            steps {
                mvn compile
            }
        }
         stage('Junit') {
            steps {
                mvn test
            }
        }
         stage('deploy') {
            steps {
                echo 'deploy steps'
            }
        }
    }
}
