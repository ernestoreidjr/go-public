pipeline {
    agent {
        kubernetes {
        cloud 'kubernetes'
        }
    }
    stages {
        stage('SonarQube') {
            steps {
                withSonarQubeEnv(installationName: 'sq-dev') { 
                    sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
                }
            }
        }
    }
}
