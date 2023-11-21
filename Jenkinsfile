pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                sh "./gradlew build"
            }
        }
        stage("Test") {
            steps {
                sh "./gradlew check"
            }
        }
    }

    post {
        always {
            junit "build/reports/**/*.xml"
            archiveArtifacts artifacts: "build/libs/**/*.jar", fingerprint: true
        }
    }
}
