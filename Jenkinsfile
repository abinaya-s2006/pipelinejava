pipeline {
    agent any

    stages {

        stage('git') {
            steps {
               sh 'git credentialsId: 'githup_creds', url: 'https://github.com/abinaya-s2006/pipelinejava.git''
                echo "git successfull"
            }
        }

        stage('build') {
            steps {
                sh 'mvn clean package'
                echo "mvn initialized"
            }
        }

        stage('Run') {
            steps {
                sh 'java -cp target/classes app'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployed successfully on AWS EC2'
            }
        }
    }
}
