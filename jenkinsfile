pipeline {
    agent any

    triggers {
        pollSCM ('* * * * *')
    }
    
    stages {
        stage('Branch') {
            steps {
                echo "$BRANCH_NAME"
            }
        }
    }
}
