
pipeline {
    agent any
    stages {
        stage('start') {
            steps {
                echo "execute something"
                sh "ls"
                sh "sleep 30"
                //publishChecks name: 'example', title: 'Pipeline Check', summary: 'check through pipeline', text: 'you can publish checks in pipeline script', detailsURL: 'https://github.com/jenkinsci/checks-api-plugin#pipeline-usage'
            }
        }
        stage('build') {
            steps {
                echo "execute something"
                sh "ls"
                sh "sleep 30"
                publishChecks name: 'example', title: 'Pipeline Check', summary: 'check through pipeline', text: 'you can publish checks in pipeline script', detailsURL: 'https://github.com/jenkinsci/checks-api-plugin#pipeline-usage'
                sh "sleep 30"
            }
        }
    }
}
