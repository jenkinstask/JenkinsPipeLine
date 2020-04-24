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
         sh 'sshpass -p Jenkins scp -o StrictHostKeyChecking=no webapp/target/*.war root@104.154.16.83:/opt/tomcat/tomcat/webapps/'
      }
   }
    }
}
