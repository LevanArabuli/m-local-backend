pipeline {
    agent any
    parameters {
        booleanParam(name: 'DEPLOY_TO_VIP', defaultValue: false, description: 'Deploy frontend and graphql to VIP repos')
    }
    stages {
        stage('Build') {
            when {
                expression {
                    BRANCH_NAME ==~ /(master|develop)/ && params.DEPLOY_TO_VIP == true
                }
            }            
            steps {
                withCredentials([usernameColonPassword(credentialsId: 'd27d46c6-9296-48aa-85e8-0d3b7fcdf8ae', passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME')]) {
                    sh "git --version"

                    //sh 'git remote add vip https://${GIT_USERNAME}:${GIT_PASSWORD}@github.com/sadamia/m-remote-frontend.git'
                    //sh 'git fetch vip'
                
                    //sh 'git reset --hard'
                    //sh 'git checkout -b develop-built vip/develop-built'

                    //sh 'git merge -X theirs origin/develop'
                    
                    //sh 'yarn build-ci'
                    //sh 'git add build -f'
                    
                    //sh 'git commit -m "branch: ${GIT_BRANCH}; commit: ${GIT_COMMIT}; BUILD_NUMBER: ${BUILD_NUMBER};"'
                    //sh 'git push vip develop-built'                
                    //sh 'echo "Start"'
                }
                echo "${params.DEPLOY_TO_VIP}"
            }
        }
    }
}
