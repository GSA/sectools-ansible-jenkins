pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                sh 'mkdir sectools-ansible-jenkins'
                sh 'mv * sectools-ansible-jenkins || echo ""'
                sh 'ansible-playbook --syntax-check sectools-ansible-jenkins/tests/test.yml'
            }
        }
    }
}