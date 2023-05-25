pipeline {
    agent any
    environment {
        PATH+EXTRA = '/usr/local/maven/bin'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
