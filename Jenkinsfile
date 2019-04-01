pipeline {
    agent none
    parameters {
        booleanParam(name: 'DEPLOY_TO_VIP', defaultValue: false, description: 'Deploy to VIP')
        string(name: 'TEST', defaultValue: 'Jenkins', description: 'Who should I say hello to?')
    }
    stages {
        stage('Build') {
            when {
                expression {
                    BRANCH_NAME ==~ /(master|develop)/
                }
            }            
            steps {
                echo "${params.DEPLOY_TO_VIP}"
                echo "${env.TEST}"
                echo "${params.TEST}"
            }
        }
    }
}
