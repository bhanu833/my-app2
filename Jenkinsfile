pipeline {
    agent {
  label 'jenkins-master'
}


    stages {
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
         stage('Junit') {
            steps {
                sh 'mvn test'
            }
        }
         stage('deploy') {
            steps {
                echo 'deploy steps'
            }
        }
    }
}
