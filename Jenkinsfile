pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh '''
                cd jenkins
                mvn clean install -DskipTests
                echo "Building" 
                '''
            }
        }
        stage('Test') { 
            steps {
                echo "Testing" 
            }
        }
        stage('Deploy') { 
            steps {
               echo "Deploy" 
            }
        }
    }
}