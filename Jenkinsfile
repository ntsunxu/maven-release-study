pipeline {
    agent any
    tools {
        jdk 'openjdk11'
    }
    stages {
        stage('mvn') {
            steps {
                withMaven(maven: 'maven3') {
                    sh 'mvn clean'
                    sh 'mvn sonar:sonar -Dsonar.projectKey=sunxuia_maven-release-study -Dsonar.organization=sunxuia -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=0e222f7440470450dc5da6dac1190342b666aba9'
                    sh 'mvn test'
                }
            }
        }
    }
}
