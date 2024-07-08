pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
         stage('Git pull') { 
            steps {
                git credentialsId: 'c3436b70-91c2-41fb-ab87-9ec084ed3484', url: 'https://github.com/JiangYue-git/simple-node-js-react-npm-app.git'
                echo '拉取成功'
            }
        }
        stage('Build') { 
            steps {
                sh 'npm -v' 
            }
        }
    }
}