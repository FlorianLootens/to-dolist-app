node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker sto to-dolist-app'
            sh 'docker rm to-dolist-app'
        }
    }
    stage('Build') {
        build 'BuildTo-DoApp'
    }
}
