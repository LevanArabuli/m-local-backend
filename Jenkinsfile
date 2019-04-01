pipeline {
    agent any
    parameters {
        booleanParam(name: 'DEPLOY_TO_VIP', defaultValue: false, description: 'Deploy frontend and graphql repos to VIP')
    }
    stages {
        stage('Build') {
          
            steps {
                echo "${params.DEPLOY_TO_VIP}"
            }
        }
    }
}
