node('maven') {
   stage('checkout sandbox-sonar')
   git url: 'https://github.com/dmarley/sandbox-sonar.git'
   
   stage('list root dir')
   sh 'ls -l -srt'

   stage('change to working dir')
   dir('java-gradle-simple'){
       stage('list dir')
       sh 'ls -l -srt'
   
       stage('execute sonar')
       sh './gradlew sonarqube -Dsonar.host.url=http://sonarqube-mem-tfrs-tools.pathfinder.gov.bc.ca -Dsonar.verbose=true --stacktrace'
   }
}
