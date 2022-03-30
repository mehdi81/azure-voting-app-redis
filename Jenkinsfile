pipeline {
    agent any

    triggers {
        pollSCM ('* * * * *')
    }
    
    stages {
        stage('Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
    }
}
