pipeline {
    agent {
        docker { image 'geektechstuff/ansible_container:latest' }
    }
    stages {
        stage('test') {
            steps {
                sh 'rm -rf sectools-ansible-jenkins || echo ""'
                sh 'mkdir sectools-ansible-jenkins || echo ""'
                sh 'mv -f * sectools-ansible-jenkins || echo ""'
                sh 'ansible-playbook --syntax-check sectools-ansible-jenkins/tests/test.yml'
            }
        }
    }
}