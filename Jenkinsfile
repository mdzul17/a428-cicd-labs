node {
    docker.image('node:16-buster-slim').withRun('-p 3000:3000') {
        stage('Build') {
            sh 'node -v'
            sh 'npm -v'
            sh 'npm install'
        }
        stage('Test'){
            sh './jenkins/scripts/test.sh'
        }
    }
}