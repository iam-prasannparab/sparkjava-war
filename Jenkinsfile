pipeline {
    agent external

    environment {
        PATH = "/opt/maven/bin:$PATH"
    }

    stages {

        stage('Clone') {
            steps {
                git url: 'https://github.com/iam-prasannparab/sparkjava-war.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
