#!groovy
pipeline{
	agent none
	stages{
		stage('code fetch'){
			steps{
				sh git clone https://github.com/ansarpalakottal/ansible.git
			}
		}
		stage('Build artifacts'){
			steps{
				echo "Building artifacts"
			}
		}
		stage('Push Artifacts'){
			steps{
				echo "Pushing Artifacts"
			}
		}
		stage('Code Deploy'){
			steps{
				ansible-playbook -i localhost debug.yml
			}
		}
	}
}
