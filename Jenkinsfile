pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/rajatrokde/jenkins.git'


                    
            }
        }

        stage('demo') {
            steps {
                sh """
                docker build -t -p 80:80 nginx 
                """
            }
        }

        stage('Deploy') {
            steps {
                sh """
                sudo cp -r * /var/www/html/
                """
            }
        }

    }
}
