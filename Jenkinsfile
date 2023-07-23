pipeline {
    agent { label 'openjdk-8'}
    triggers { pollSCM('* * * * *') }
stages { 
    stage('vcs') {
        steps {
            git branch: 'developer',
                url: 'https://github.com/sridharkomati/jenkins.july24.git'
        }
    stage('build') {
        steps {
            sh 'ls'
            sh 'java -version' 
            sh 'mvn --version'
        }
    }    
   }
}
}
