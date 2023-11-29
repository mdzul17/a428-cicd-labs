node {
    docker.image('node:16-buster-slim').withRun('-p 3000:3000') {
        stage('Build') {
            // Inside the stage block, you can have multiple steps
            // This is equivalent to the "steps" block in Declarative Pipeline
            sh 'npm install'
        }
        stage('Test'){
            sh './jenkins/scripts/test.sh'
        }
    }
}