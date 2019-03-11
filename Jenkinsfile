 pipeline {
    agent	any
    stages {
        stage('To test') { 
            steps {
				echo " This is for test of pipeline ..... This is BY Siddharth!!" 
            	}
        	}
			stage('Indexfile deployment') { 
            steps {
				sh "cd /var/lib/jenkins/workspace/SidDocker/"
                sh "cp -R index.html /var/www/html/"
				echo " This is for Copt index file" 
				}
			}
			stage('Docker deployment') { 
            steps {
                sh "docker build -t webserver:v1 ."
				sh "docker run -d -p 80:80 webserver:v1"
                echo " This is from docker file" 
				}
			}			
    	}
	}