pipeline {
    agent any
    parameters {
        booleanParam(name: 'DEPLOY_TO_VIP', defaultValue: false, description: '')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Start"'
                sh 'sleep 15'
                echo "${params.DEPLOY_TO_VIP} World!"
                sh 'echo "End"'
            }
        }
    }
}
