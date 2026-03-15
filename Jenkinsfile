pipeline {
    agent any

    stages {

        stage('Clone the repo') {
            steps {
                git branch: 'main', url: 'https://github.com/rajatrokde/jenkins.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo " rajat"
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker run -d -p 80:80 --name nginx1 my-nginx
                docker run -d -p 81:80 --name nginx2 my-nginx
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo cp -r * /var/www/html/
                '''
            }
        }

    }
}
