pipeline {
    agent any
    options {
        durabilityHint ‘PERFORMANCE_OPTIMIZED’
        }
    stages {
        stage (‘Build’) {
            steps {
                sh ‘mvn clean package’
                }
            }
        }

