pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/muneebmoon/Devops-Project.git'
            }
        }

        stage('Deploy to Azure VM') {
            steps {
                script {
                    // Use sshpass to copy files to remote Azure VM
                    sh '''
                    sshpass -p 'Ahmed1234!@#$' scp -o StrictHostKeyChecking=no -r * ahmed@135.235.136.184:/var/www/html
                    '''
                }
            }
        }
    }
}
