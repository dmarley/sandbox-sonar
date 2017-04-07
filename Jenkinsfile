node('maven') {

   stage('checkout navUnit')
   git url: 'https://github.com/dmarley/tfrs-sonar-scanner.git'

   stage('change to working dir')
   dir 'java-gradle-simple'
   
   stage('execute sonar')
   sh './gradlew sonarqube -Dsonar.jdbc.url=jdbc:postgresql://postgresql/sonar -Dsonar.verbose=true -Dsonar.jdbc.username=user7IO -Dsonar.jdbc.password=gnWBsreWQ7A0HXXU'


}
