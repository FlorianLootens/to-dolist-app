node {
    triggers {
        githubPush() // automatisch bouwen bij GitHub push
    }
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS!!') {
            sh 'docker rm -f to-dolist-app || true'
        }
    }
    stage('Build') {
        build 'BuildTo-DoApp'
    }
}
