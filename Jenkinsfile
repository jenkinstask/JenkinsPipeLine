pipeline {
    agent any
    stages {
        stage ('SCM checkout') {
            steps {
                git credentialsId: 'GITHUB_USER', url: 'https://github.com/jenkinstask/JenkinsPipeLine.git'
                }
        }

        stage ('Maven Build') {
            steps {
                sh 'mvn clean package' 
            }
            
        }
	//	stage('Deploy to Tomcatrt'){
     //    steps(['tomcat-dev']) {
     //    sh 'sshpass -p Jenkins scp -o StrictHostKeyChecking=no webapp/target/*.war root@34.68.179.70:/opt/tomcat/webapps/'
		 
     // }
   //}
        }
   
    }
