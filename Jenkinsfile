node {
    stage('SCM') {
        git 'https://github.com/satishnbtech/tester.git'
    }
    stage('Build & Package'){
        sh label: '', script: 'mvn package'
    }
    
    stage('Results'){
       archive 'gameoflife-web/target/gameoflife.war' 
       junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}
