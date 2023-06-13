library 'Jenkins DSL Library'

pipeline {
    agent any
    stages {
        stage ('Checkout') {
            agent {label 'agent'}
            steps {
                script {
                    echo "test"
                }
                pipelineMaven(['skipTests' : true, 'skipInstall': false])
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
