pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/YOUR_USERNAME/repo.git',
                branch: "${BRANCH_NAME}"
            }
        }

        stage('Inject Branch Name') {
            steps {
                sh """
                sed -i 's/BRANCH_NAME/${BRANCH_NAME}/g' script.js
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
