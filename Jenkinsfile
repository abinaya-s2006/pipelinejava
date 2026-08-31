pipeline {
    agent any

    tools {
        // Must match the names configured in Jenkins Global Tool Configuration
        maven 'Maven 3.x'
        jdk   'JDK 17'
    }

    stages {
        stage('Checkout Source') {
            steps {
                // Pulls source code from your version control system
                checkout scm
            }
        }

        stage('Build & Package') {
            steps {
                // Compiles code, runs tests, and builds the target JAR file
                withMaven(maven: 'Maven 3.x') {
                    sh 'mvn clean package'
                }
            }
        }

        stage('Execute Program') {
            steps {
                // Runs the compiled Hello World executable JAR file
                sh 'java -jar target/pipeline {
    agent any

    tools {
        // Must match the names configured in Jenkins Global Tool Configuration
        maven 'Maven 3.x'
        jdk   'JDK 17'
    }

    stages {
        stage('Checkout Source') {
            steps {
                // Pulls source code from your version control system
                checkout scm
            }
        }

        stage('Build & Package') {
            steps {
                // Compiles code, runs tests, and builds the target JAR file
                withMaven(maven: 'Maven 3.x') {
                    sh 'mvn clean package'
                }
            }
        }

        stage('Execute Program') {
            steps {
                // Runs the compiled Hello World executable JAR file
                sh 'java -jar target/AWS-1.0-SNAPSHOT.jar'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check build logs.'
        }
    }
}.jar'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check build logs.'
        }
    }
}
