pipeline {
    agent {
        label "!windows"
    }
    environment {
        DB_ENGINE = "sqlite"
        DISABLE_AUTH = "true"
    }
    stages {
        stage("Build") {
            steps {
                echo "DB_ENGINE is ${DB_ENGINE}"
                echo "DISABLE_AUTH is ${DISABLE_AUTH}"
                sh "printenv"
            }
        }
    }
}
