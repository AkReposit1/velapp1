pipeline{

	agent{
		label{
			label 'Slave3'
			customWorkspace '/home/ec2-user/22Q3'
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
				sh"sudo service httpd start"
				sh"sudo chkconfig httpd on"
                        }
                }
		stage('deploy index.html on httpd'){
                        steps{
                                echo "deploying imdex.html"
				sh"sudo cp -r /home/ec2-user/22Q3/index.html /var/www/html/"
				sh"sudo chmod -R 777 /var/www/html/"
                        }
                }
	}

}
