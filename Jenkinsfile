pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2 -v /root/devops/maven/settings.xml:/usr/share/maven/conf/settings.xml'
        }
    }
    stages {
        stage('Back-Build') { 
            steps {
                sh 'cat /usr/share/maven/conf/settings.xml'
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
