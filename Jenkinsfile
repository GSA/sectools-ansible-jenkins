pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                sh 'ls && cd ../ && ansible-playbook --syntax-check sectools-ansible-jenkins/tests/test.yml'
            }
        }
    }
}