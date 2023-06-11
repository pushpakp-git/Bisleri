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
							sh '/home/dev/apache-maven-3.9.1/bin/mvn install'
							}
						}
						
			stage('Deployment') {
						steps {
							sh 'cp target/Bisleri.war /home/dev/apache-tomcat-9.0.73/webapps'
							}
						}
			}
		}
