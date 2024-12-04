pipeline {
    agent {
  label 'jenkins-master'
}


    stages {
        stage('compile') {
            steps {
                powershell 'mvn compile'
            }
        }
         stage('Junit') {
            steps {
               powershell 'mvn test'
            }
        }
        stage('package') {
            steps {
               powershell 'mvn -DskipTests clean package'
            }
        }
         stage('clean workspace') {
            steps {
                cleanWs()
            }
        }
    }
}
