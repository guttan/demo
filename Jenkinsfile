pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M2_HOME"
    }

    stages {
        stage('Build') {
            steps {
                git 'git@github.com:guttan/demo.git'

                sh "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
}
