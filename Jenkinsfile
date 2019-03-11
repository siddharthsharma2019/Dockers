 pipeline {
    agent any 
    stages {
        stage('To test') { 
            steps {
				echo " This is for test of pipeline ..... This is BY Siddharth!!" 
            	}
        	}
			stage('Indexfile deployment') { 
            steps {
				sh "cd /var/lib/jenkins/workspace/SidDocker/"
                sh "sudo yum -y install httpd"
				sh "cp -R index.html /var/www/html/"
				echo " This is for Copt index file" 
				}
			}
			stage('Docker deployment') { 
            steps {
                sh "docker build -t webserver:v1 ."
                echo " This is from docker file" 
				}
			}			
    	}
	}