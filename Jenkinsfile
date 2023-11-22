pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage("Deploy Staging") {
            steps {
                sh "./deploy staging"
                sh "./run-smoke-tests"
            }
        }
        stage("Sanity Check") {
            steps {
                input "Does the staging environment look ok?"
            }
        }
        stage("Deploy Production") {
            steps {
                sh "./deploy production"
            }
        }
    }
}
