pipeline {
    agent any

    stages {
        stage('scm') {
            steps {
                git branch: 'war', url: 'https://github.com/Santoz0012/Maven-project.git'
            }
        }
    stage('build') {
            steps {
               sh 'mvn clean'
               sh 'mvn install'
            }
        }
     stage('deploy') {
            steps {
              sh 'cp -rp "/var/lib/jenkins/workspace/pipe-demo/target/my-web.war" "/opt/apache-tomcat/webapps"'
            }
        }            
    }
}
