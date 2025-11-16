pipeline{
    agent any
    tools{
        maven 'maven'
    }
    stages{
        stage('git chkout'){
            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/NamanUM/addressbook.git']])
            }
        }
        stage('build project'){
            steps{
                sh 'mvn compile'
            }
        }
    }
}
