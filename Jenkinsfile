pipeline {
    agent any
    properties([parameters([booleanParam(defaultValue: false, description: '', name: 'DEPLOY_TO_VIP')])])
    stages {
        stage('Build') {
            steps {
                sh 'echo "Start"'
                sh 'sleep 15'
                sh 'echo "End"'
            }
        }
    }
}
