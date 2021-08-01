pipeline {
    agent any

    stages {
        stage('Clone-Repo') {
            steps {
                echo 'Cloning..'
                sh 'git clone 'https://github.com/indraindrajit71/mavendevops.git
                sh 'mvn clean /var/lib/jenkins/workspace/my-app'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mvn test /var/lib/jenkins/workspace/my-app'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'mvn package /var/lib/jenkins/workspace/my-app'
            }
        }
    }
}

