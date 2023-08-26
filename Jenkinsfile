pipeline{
    agent any

    stages{
      stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], 
                          userRemoteConfigs: [[url: 'https://github.com/shailednrapali/spring-petclinic.git']]])
            }
        }
        
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
