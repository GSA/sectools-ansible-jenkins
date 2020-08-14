pipeline {
    agent { docker { image 'ansible' } }
    stages {
        stage('test') {
            steps {
                sh 'ansible-playbook --syntax-check tests/test.yml'
            }
        }
    }
}