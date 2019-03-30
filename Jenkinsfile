pipeline {
    agent any
    parameters {
        booleanParam(name: 'DEPLOY_TO_VIP', defaultValue: false, description: '')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Start"'
                echo "${params.DEPLOY_TO_VIP}"
                sh 'echo "End"'
            }
        }
    }
}
