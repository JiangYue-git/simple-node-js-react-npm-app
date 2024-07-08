pipeline {
     agent {
        docker { image 'node:7-alpine' }
    }
     tools{
        maven 'maven'
        jdk 'jdk'
    }
    stages {
         stage('git pull') { 
            steps {
                git credentialsId: 'c3436b70-91c2-41fb-ab87-9ec084ed3484', url: 'https://github.com/JiangYue-git/simple-node-js-react-npm-app.git'
                echo '拉取成功'         
            }
        }
         stage('build') { 
            steps {
                sh "node -v"   
                sh "npm install --registry=https://registry.npmmirror.com"
            }
        }
    }
}