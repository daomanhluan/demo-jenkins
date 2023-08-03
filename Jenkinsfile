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
			sh '''
			cd jenkins/target/
			java -jar jenkins-0.0.1-SNAPSHOT.jar
               echo "Deploy" 
			   '''
            }
        }
    }
}