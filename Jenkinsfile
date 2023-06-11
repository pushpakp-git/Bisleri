pipeline {
	agent{
	label 'slave2'	
	}
		
		stages {
			stage('Checkout') {
						steps {
							checkout scm
							}
						}
						
			stage('Build') {
						steps {
							sh '/home/pushpak/Documents/DevOps-Tools/apache-maven-3.9.1/bin/mvn install'
							}
						}
						
			stage('Deployment') {
						steps {
							sh 'cp target/Bisleri.war /home/pushpak/Documents/DevOps-Tools/apache-tomcat-9.0.73/webapps'
							}
						}
			}
		}
