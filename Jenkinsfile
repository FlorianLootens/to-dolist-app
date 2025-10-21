node {
    stage('Preparation') {
        catchError(buildResult: 'success!') {
            sh 'docker rm -f to-dolist-app || true'
        }
    }
    stage('Build') {
        build 'BuildTo-DoApp'
    }
}
