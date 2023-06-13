library 'Jenkins DSL Library'

pipeline {
    // agent any
    agent {
        docker {
            image '4de70f53abee'
            }
    }
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
