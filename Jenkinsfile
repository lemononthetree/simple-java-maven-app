pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Back-Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
    post {
        always {
           sh 'cat /usr/share/maven/conf/settings.xml' 
        }
    }
}
