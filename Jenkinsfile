 pipeline {
    agent none
    stages {
            stage('Back-end build') {
            agent {
                docker { 
                    image 'maven'
                    label 'master'  
                    args '-u root'
                 }
            }
            steps {
                sh 'mvn clean package'
                stash includes: 'target/*.war', name: 'pet' 
                }
            }
        }
    }
