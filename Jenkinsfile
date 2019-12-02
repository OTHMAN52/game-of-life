node {
    stage('SCM') {
        git 'https://github.com/OTHMAN52/game-of-life.git'
    }
    
    stage('Build and package') {
        sh label: '', script: 'mvn package'
    }
    
    stage('Result') {
        archive 'gameoflife-web/target/gameoflife.war'
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
    
    
}