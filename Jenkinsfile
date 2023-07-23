pipeline {
    agent { lables 'openjdk-8'}
    options {
        timeout(time: 1, unit: 'HOURS')
        triggers { pollSCM('* * * * *') }
}
stages { 
        stage('git') {
            steps {
                git branch: 'develop',
                    url: 'https://github.com/wakaleo/game-of-life.git'
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