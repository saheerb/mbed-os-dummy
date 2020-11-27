
pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "execute something"
                sh "ls"
                publishChecks name: 'example', title: 'Pipeline Check', summary: 'check through pipeline', text: 'you can publish checks in pipeline script', detailsURL: 'https://github.com/jenkinsci/checks-api-plugin#pipeline-usage'
            }
        }
    }
}
