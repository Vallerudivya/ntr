pipeline {
    agent any

    stages {
        stage('cd') {
            steps {
                git 'https://github.com/kliakos/sparkjava-war-example.git'
            }
        }
        stage('cb') {
            steps {
                sh 'mvn install'
            }
        } 
       stage('c dep') {
            steps {
                sh 'sshpass -p "divya" scp target/sparkjava-hello-world-1.0.war root@172.17.0.3:/var/lib/apache-tomcat-9.0.56/webapps'
            }
        } 
    }
}

