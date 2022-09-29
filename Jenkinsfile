pipeline{

	agent{
		label{
			label 'Slave1'
			customWorkspace '/home/ec2-user/22Q1'
		}
	}
	
	stages{
	
		stage('install httpd'){
			steps{
				echo "Installing httpd"
				sh"sudo yum install httpd -y"
			}
		}
		stage('start httpd'){
                        steps{
                                echo "Start httpd"
				sh"sudo service start httpd"
				sh"sudo chkconfig httpd on"
                        }
                }
		stage('deploy index.html on httpd'){
                        steps{
                                echo "deploying imdex.html"
				sh"cp -r /home/ec2-user/22Q1/index.html /var/www/html/"
				sh"chmod -R /var/www/html/"
                        }
                }
	}

}
