pipeline {
    agent {
        docker { image 'ansible/ansible:default' }
    }
    stages {
        stage('test') {
            steps {
                sh 'mkdir sectools-ansible-jenkins || echo ""'
                sh 'mv -f * sectools-ansible-jenkins || echo ""'
                sh 'apk add --no-cache --purge -uU ansible ansible-lint sudo curl ca-certificates openssh-client'
                sh 'ansible-playbook --syntax-check sectools-ansible-jenkins/tests/test.yml'
            }
        }
    }
}