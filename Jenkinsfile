spipeline {
    agent {
        label 'linux'
    } 
    stages {
        stage('git pull') {
            steps {
                git branch: 'main', credentialsId: '4f9fa63b-443b-4486-8cae-8f79079d62d9', url: 'git@github.com:gnoy4eg/vector-role.git'
            }
        }
        stage('molecule test') {
            steps {
                sh 'molecule test -s centos'
            }
        }
    }
} 
