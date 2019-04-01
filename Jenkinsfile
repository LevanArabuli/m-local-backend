pipeline {
    agent any

    stages {
        stage('Build') {
            when {
                expression {
                    BRANCH_NAME ==~ /(master|develop)/
                }
            }           
            steps {
                echo "hi"
            }
        }
    }
}
