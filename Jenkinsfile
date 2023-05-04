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
        stage (‘Test’) {
            parallel {
                    stage (‘Unit Test’) {
                        steps {
                            sh ‘mvn test’
                        }
                    }
                    stage (‘Integration Test’) {
                        steps {
                            sh ‘mvn verify’
                        }
                    }
            }
    }
    stage (‘Deploy’) {
        steps {
            sh ‘mvn deploy’
            }
            }
             }
              }

