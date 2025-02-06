pipeline{
    agent any

    tools {
        maven 'test-maven'
    }
    
    stages{

        stage('build stage'){
            steps{
                sh 'mvn clean package'
            }
            post {
              success {
                    archiveArtifacts artifacts: '**/target/*.war'
                  }
            }            
        }
    }
}
