pipeline{
	agent none
	stages{
		stage('Non-Parallel Stage'){
			agent{
				label 'parallelNode'
			}
			steps{
				echo "This stage will be executed first"	
			}
		}

		stage('Run Tests'){
			parallel{
				stage('test on Windows'){
					agent{
						label 'jenkinsNode'
					}
					steps{
						echo 'Task1 on Agent'
					}
				}
				
				stage('Test on arbaaz'){
					agent{
						label 'parallelNode'
					}
					steps{
						echo ' Task1 on Agent2'
					}
				}
			}
		}	
	}
}
