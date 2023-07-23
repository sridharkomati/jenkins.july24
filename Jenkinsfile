pipeline {
    agent { label 'openjdk-8'}
    timeout(time: 1, unit: 'HOURS')
    triggers { pollSCM('* * * * *') }
}
stages { 
    stage('git') {
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
