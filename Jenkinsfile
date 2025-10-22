pipeline {
    agent any

    triggers {
        githubPush() // automatisch bouwen bij GitHub push
    }

    stages {
        stage('Preparation') {
            steps {
                catchError(buildResult: 'success') {
                    sh 'docker stop to-dolist-app'
                    sh 'docker rm to-dolist-app'
                }
            }
        }

        stage('Build') {
            steps {
                build 'BuildTo-DoApp'
            }
        }
    }
}
