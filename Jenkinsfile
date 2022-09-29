pipeline{

	agent any
	
	stages{
	
		stage('stage-1'){
			steps{
				echo "This is master Stage-1"
				sh"touch stage1"
			}
		}
		stage('stage-2'){
                        steps{
                                echo "This is master Stage-2"
			sh"touch stage2"
                        }
                }
		stage('stage-3'){
                        steps{
                                echo "This is master Stage-3"
				sh"touch stage3"
                        }
                }
	}

}
