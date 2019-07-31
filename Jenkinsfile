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
                    sh 'mvn test'
                }
            }
        }
    }
}
