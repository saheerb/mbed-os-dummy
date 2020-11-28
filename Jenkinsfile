
pipeline {
    agent any
    stages {
        stage('start') {
            steps {
                echo "execute something"
                script {
                    text = """
| Area       | KPI                      | What's it |   |
|------------|--------------------------|-----------|---|
| Defects    | Customer defects         |           |   |
|            | Defect %                 |           |   |
|            | Critical/Blocker defects |           |   |
|            | Code Coverage            |           |   |
|            | Burn down                |           |   |
|            | Epic burn down           |           |   |
|            | Velocity                 |           |   |
|            | Control Chart            |           |   |
| Automation | % of automated tests     |           |   |
| Automation | Flaky tests              |           |   |
| Automation | Time to execute          |           |   |
| CI Quality | Broken builds            |           |   |
|            |                          |           |   |
                    """
                }
                sh "ls"
                sh "sleep 3"
                publishChecks conclusion: 'FAILURE',detailsURL: 'http://google.com', name: 'test', status: 'IN_PROGRESS', summary: 'Summary ', text: text, title: 'title of something'
                //publishChecks name: 'example', title: 'Pipeline Check', summary: 'check through pipeline', text: 'you can publish checks in pipeline script', detailsURL: 'https://github.com/jenkinsci/checks-api-plugin#pipeline-usage'
            }
        }
        stage('build') {
            steps {
                echo "execute something"
                sh "ls"
                sh "sleep 30"
                publishChecks detailsURL: 'http://google.com', name: 'test', summary: 'Summary ', text: 'one test', title: 'title of something'
                publishChecks name: 'example', title: 'Pipeline Check', summary: 'check through pipeline', text: 'you can publish checks in pipeline script', detailsURL: 'https://github.com/jenkinsci/checks-api-plugin#pipeline-usage'
                sh "sleep 3"
            }
        }
    }
}
