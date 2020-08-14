pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                sh 'cd ../ && ansible-playbook --syntax-check sectools-ansible-jenkins/tests/test.yml'
            }
        }
    }
}