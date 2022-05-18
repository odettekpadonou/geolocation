pipeline {
    triggers {
  polISCM '* * * * *'
}
    agent any
    tools {
  maven "M2"
    }

    stages {
        stage('maven package') {
            steps {
               sh 'mvn clean'
               sh 'mvn install'
               sh 'mvn package'
            }
        }
         stage('build') {
            steps {
                echo 'build'
            }
        }
         stage('test') {
            steps {
                sh 'mvn test'
            }
        }
         stage('deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
}

