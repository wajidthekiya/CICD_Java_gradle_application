pipeline{
    agent any
    stages{
        stage("Sonar_Quality_Check"){
            agent {
                docker {
                    image "openjdk:11"
                }
            }
            steps{
                script {
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                        sh " chmod +x gradlew "
                        sh " ./gradlew sonarqube "
    
                   }
 
                }
            }
            
        }
    }
    
}
