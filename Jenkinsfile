pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                sh 'mkdir sectools-ansible-jenkins && mv !(sectools-ansible-jenkins) sectools-ansible-jenkins && ansible-playbook --syntax-check sectools-ansible-jenkins/tests/test.yml'
            }
        }
    }
}