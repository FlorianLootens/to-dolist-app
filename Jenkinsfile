node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker stop TODO'
            sh 'docker rm TODO'
        }
    }
    stage('Build') {
        build 'BuildTo-DoApp'
    }
}
