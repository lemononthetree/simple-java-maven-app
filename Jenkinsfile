pipeline {
    agent any
    environment {
        PATH = '$PATH:/usr/local/maven/bin'
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
