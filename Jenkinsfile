pipeline {
    triggers {
  pollSCM('* * * * *')
}
    agent any
    tools {
  maven 'M2'
}
    

    stages {
        stage('maven package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
          stage('test') {
            steps {
                sh 'test'
                
            }
        }
         
          stage('deploy') {
            steps {
                echo 'deploy'
                
           }
                
        }

    }
}

         

        
        
    
    

