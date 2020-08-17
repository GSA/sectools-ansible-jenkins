pipeline {
    agent {
        docker { image 'ansible/ansible:default' }
    }
    stages {
        stage('test') {
            steps {
                sh 'ls'
                sh 'rm -rf sectools-ansible-jenkins || echo ""'
                sh 'mkdir sectools-ansible-jenkins || echo ""'
                sh 'mv -f * sectools-ansible-jenkins || echo ""'
                sh 'ls'
            }
        }
    }
}