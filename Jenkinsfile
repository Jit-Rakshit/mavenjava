pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        /*stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }*/
        stage('Deliver') {
            steps {
                sh 'java -jar /var/lib/jenkins/workspace/Gitmaven/target/myapp-1.0-SNAPSHOT.jar'
            }
        }
    }
}
