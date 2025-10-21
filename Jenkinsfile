node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker rm -f todo-app || true'
        }
    }
    stage('Build') {
        build 'BuildTo-DoApp'
    }
}
