pipeline {
    agent any


        stages {
           stage ('Build') {
            steps {
                sh 'mvn clean install package' 
            }
         }
	stage('Deploy to Tomcat'){
         steps(['tomcat-dev']) {
         sh 'sshpass -p Jenkins scp -o StrictHostKeyChecking=no webapp/target/*.war root@35.192.53.22:/opt/tomcat/tomcat/webapps/'
      }
   }
    }
}
