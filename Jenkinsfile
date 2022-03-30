pipeline {
    agent any

    triggers {
        pollSCM ('* * * * *')
    }
    
    stages {
/**        stage('Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }**/

        stage('Docker Build'){
            steps {
                pwsh(script: 'docker images -a')
                pwsh(script: """
                    cd azure-vote/
                    docker images -a
                    docker build -t- jenkins-pipeline .
                    docker images -a
                    cd ..
                """
                )
            }
        }
    }
}
