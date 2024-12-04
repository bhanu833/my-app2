pipeline {
    agent {
  label 'jenkins-master'
}
timestamps {
    // some block
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
        stage('upload package to nexus') {
            steps {
               powershell 'mvn -DskipTests deploy'
            }
        }
         stage('clean workspace') {
            steps {
                cleanWs()
            }
        }
    }
}
