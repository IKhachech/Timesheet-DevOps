pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/master']],
                    userRemoteConfigs: [[url: 'https://github.com/IKhachech/Timesheet-DevOps.git']]
                ])
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
    }
}
