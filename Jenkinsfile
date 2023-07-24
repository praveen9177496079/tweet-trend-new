pipeline {
    agent {
        node {
            label 'maven'
        }
    }
environment {
    PATH = "/opt/apache-maven-3.9.3/bin:$PATH"
}    

    stages {
        stage('Build Stage') {
            steps {
                sh 'mvn clean deploy'
            }
        }

        stage('SonarQube analysis') {
        enviroment {    
          scannerHome = tool 'sonar-scanner'
        }
          steps {
            withSonarQubeEnv('sonarqube-server') { // If you have configured more than one global server connection, you can specify its name
              sh "${scannerHome}/bin/sonar-scanner"
        
            }     
        } 
    }
}

