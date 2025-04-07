pipeline {
    agent any

    stages {
        stage('check code ') {
            steps {
                checkout scm 
            }
        }
        
        stage('Build  Application') {
            agent {
                docker {
                    image 'python:3.9'  // 使用 Go 1.19 镜像来构建应用
                    reuseNode true
                }
            }
            steps {
                echo 'Building application...'
                sh 'pip install -r requirements.txt'    // 安装依赖
            }
        }

        
        
    }
}
