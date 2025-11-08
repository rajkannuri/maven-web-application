    echo "Here is the build display name: ${env.BUILD_DISPLAY_NAME}"
	echo "Here is the build number: ${env.BUILD_NUMBER}"
	echo "Here is the Node name: ${env.NODE_NAME}"
	echo "Here is the Jenkins url name: ${env.JENKINS_URL}"
	node{
	 
	 	echo "Here is the build display name: ${env.BUILD_DISPLAY_NAME}"
	echo "Here is the build number: ${env.BUILD_NUMBER}"
	echo "Here is the build id: ${env.BUILD_ID}"   
	
	def mavenHome = tool name: 'maven 399'
	
	stage('CheckOutCode'){
	git branch: 'development', url: 'https://github.com/rajkannuri/maven-web-application.git'
	}
	
	stage('Build'){
	sh "${mavenHome}/bin/mvn clean package"
	}
	/*
	stage('Reportgeneration'){
	sh "${mavenHome}/bin/mvn clean package sonar:sonar"
	}
	stage('ArtifactsRepository'){
	sh "${mavenHome}/bin/mvn clean package deploy"
	}
		stage('Deploy app to Tomacat server'){
	sshagent(['8f0e6357-7bde-4271-ad99-aa5317e14fdd']) {
	sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/pipelinescriptedway/target/maven-web-application.war ec2-user@172.31.2.253:/opt/tomcat9/webapps/" 
	}
	}
	*/
	}
	
