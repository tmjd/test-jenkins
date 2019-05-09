#!groovy
pipeline {
    agent { label 'slave'}
    environment {
        // Jenkins job info
        SANE_JOB_NAME = "${env.JOB_BASE_NAME}".replace('.', '-').toLowerCase()

        // The docs version that we are updating.
        DOCS_VERSION="${DOCS_VERSION:-master}"
    }

    stages {
        stage('The stage') {
            steps {
                sh 'echo "The stage sees DOCS_VERSION=$DOCS_VERSION"'
            }
        }
    }

    post {
        always {
            echo "Always do stuff."
        }
        success {
            echo "Yay, we passed."
        }
    }
}
