node {
    stage('Preparation') {
        catchError(buildResult: 'success!') {
            sh 'docker stop to-dolist-app'
            sh 'docker rm to-dolist-app'
        }
    }
    stage('Build') {
        build 'BuildTo-DoApp'
    }
}
