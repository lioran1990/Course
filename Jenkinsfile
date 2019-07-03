def file_command
pipeline {
    agent {
        label 'master'
    }
    stages {
        stage('checkout'){
            steps {
                script {
                    git credentialsId: 'devopint', url: 'https://github.com/DevOpsINT/Course.git'
                }
            }
        }
        stage('shell command example') {
            steps {
                script {
                    file_command = sh script: 'echo "new file added" > newfile', returnStdout: true
                    print(file_command)
                    sh "echo file_command is ${file_command} > variable"
                    sh 'cat variable'
                }
            }
        }
    }
}
