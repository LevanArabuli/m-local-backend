pipeline {
    agent any
    parameters {
        booleanParam(name: 'DEPLOY_TO_VIP', defaultValue: false, description: 'Deploy to VIP')
    }
    stages {
        stage('Build') {
            when {
                expression {
                    BRANCH_NAME ==~ /(master|develop)/ && params.DEPLOY_TO_VIP == true
                }
            }            
            steps {
                echo "${env.DEPLOY_TO_VIP}"
            }
        }
    }
}
