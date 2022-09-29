pipeline{

	agent{
		label{
			label 'Slave2'
			customWorkspace '/home/ec2-user/22Q2'
		}
	}
	
	stages{
	
		stage('stage-1'){
			steps{
				echo "This is 22Q2 Stage-1"
				sh"touch stage1"
			}
		}
		stage('stage-2'){
                        steps{
                                echo "This is 22Q2 Stage-2"
			sh"touch stage2"
                        }
                }
		stage('stage-3'){
                        steps{
                                echo "This is 22Q2 Stage-3"
				sh"touch stage3"
                        }
                }
	}

}
