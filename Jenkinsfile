pipeline {
    agent any
    environment {
        NOME = 'Carlos'
        SOBRENOME = 'Grassi'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "${NOME}"
            }
        }        
        stage('Upload') {
            steps {
                echo 'Uploading..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'echo $SOBRENOME'
                sh 'pwd'
                sh 'ls -la'
            }
        }
        stage('Reports') {
            steps {
                echo 'Reports..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        stage('Smoke') {
            steps {
                echo 'Smoke....'
            }
        }
    }
    post {
            always {
                echo 'Sempre serei executado'
            }
            success {
                echo 'Serei executado apenas quando a pipeline fechar com sucesso'
            }
            failure {
                echo 'Serei executado apenas quando a pipeline fechar com erro'
            }
        }
}
