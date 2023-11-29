node {
    docker.image('node:16-buster-slim').withRun('-u root -p 3000:3000') {
        stage('Setup') {
            sh 'apt-get update && apt-get install -y nodejs npm'
            sh 'ln -s /usr/bin/nodejs /usr/bin/node'
            sh 'node -v'
            sh 'npm -v'
        }
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