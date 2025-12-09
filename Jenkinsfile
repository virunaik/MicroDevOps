pipeline {
    agent {
        label 'viru'
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
                git branch: 'master', url: 'https://github.com/virunaik/MicroDevOps.git'
            }
        }

        stage('Install httpd') {
            steps {
                sh 'sudo yum install -y httpd'
            }
        }

        stage('Copy files') {
            steps {
                sh 'sudo cp index.html /var/www/html/'
            }
        }
    }
}
