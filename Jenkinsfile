pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'Git_cred', url: 'https://github.com/noorwale/maven-prject.git']]])
            }
        }
        stage('build'){
            steps{
                sh 'mvn clean install'
            }
        }
    }
}
