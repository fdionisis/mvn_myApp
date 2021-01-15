pipeline {
    agent any 
    stages {
        stage('clone repo and clean it') { 
            steps {
                sh "rm -rf mvn_myApp"
                sh "git clone https://github.com/fdionisis/mvn_myApp.git"
                sh "mvn clean -f mvn_myApp"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f mvn_myApp"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f mvn_myApp"
            }
        }
    }
}
