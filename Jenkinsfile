pipeline {
    agent { label 'openjdk-8'}
    triggers { pollSCM('* * * * *') }
stages { 
    stage('vcs') {
        steps {
            git branch: 'developer',
                url: 'https://github.com/sridharkomati/jenkins.july24.git'
        }
    }    
    stage('build') {
        steps {
            sh 'ls'
            sh 'export PATH="/usr/lib/jvm/java-1.8.0-openjdk-amd64/bin:$PATH"'
            sh 'java -version' 
            sh 'mvn --version'
            sh 'mvn package'
            

        }
    }    
   }
}
