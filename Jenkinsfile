pipeline {
    agent any
    stages {
        stage('Pull') {
            steps {
                checkout([$class: 'GitSCM',
                branches: [[name: '*/main']],
                doGenerateSubmoduleConfigurations: false,
                extensions: [],
                submoduleCfg: [],
                userRemoteConfigs: [[url: 'https://github.com/Shurt91/Jenkins-Hello.git']]])
                sh "ls"
            }
        }
        stage('Build') {
            steps {
                sh "javac Main.java"
            }
        }
        stage('Run') {
            steps {
                sh "java Main"
            }
        }
    }
}
