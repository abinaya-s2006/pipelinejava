pipeline {
    agent any
    stages {
        stage('git') {
            steps {
               git credentialsId: 'githup_creds', url: 'https://github.com/abinaya-s2006/pipelinejava.git'
                echo "git successfull"
            }
        }
          stage('version') {
            steps {
                sh 'java --version'    
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean package'
                echo "mvn initialized"
            }
        }
        stage('deploy') {
            steps {
                sh 'ls -l target'
                sh 'java -jar target/AWS-1.0-SNAPSHOT.jar'
            }
        }

    }
}
