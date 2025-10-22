pipeline {
    agent any

    triggers {
        githubPush() // automatisch bouwen bij GitHub push
    }

    stages {
        stage('Preparation') {
            steps {
                catchError(buildResult: 'success') {
                    sh 'docker rm -f to-dolist-app || true'
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
