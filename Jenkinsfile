pipeline {
    agent any
    stages {
        stage("No-op") {
            steps {
                sh "ls"
            }
        }
    }

    post {
        always {
            echo "One way or another, I have finished"
            deleteDir() /* cleanup the pipeline's workspace */
        }
        success {
            echo "I succeeded!"
        }
        unstable {
            echo "I'm unstable!"
        }
        failure {
            echo "I failed!"
        }
        changed {
            echo "Things were different before!"
        }
    }
}
