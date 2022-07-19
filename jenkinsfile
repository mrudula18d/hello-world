pipeline {
    agent any
    
    environment {
        PATH = "/opt/maven/bin:$PATH"
    }

    stages {
        stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/mrudula18d/hello-world']]])
            }
        }
        
        stage('build') {
            steps {
                sh "mvn clean install"
            }
        }
    }
}
