pipeline {
    agent any
    parameters {
        booleanParam(name: 'DEPLOY_TO_VIP', defaultValue: false, description: 'Deploy to VIP')
    }
    stages {
        stage('Build') {
            when {
                expression {
                    BRANCH_NAME ==~ /(master|develop)/
                }
            }            
            steps {
                echo "${env}"
                echo "hi"
                echo "${params.DEPLOY_TO_VIP}"
            }
        }
    }
}
