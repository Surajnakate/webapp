pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: "https://github.com/Surajnakate/webapp.git"
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh "mvn  clean install"
            }
        }
    }
        post {
        success {
            // Actions to perform when the pipeline is successful
            echo 'Pipeline successful!'
            // You can add notifications or other actions here
        }
        failure {
            // Actions to perform when the pipeline fails
            echo 'Pipeline failed!'
            // You can add notifications or other actions here
        }
    }
}
