pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'export PATH=$PATH:/usr/local/maven/bin'
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
