#!groovy
pipeline{
	agent none
	stages{
		stage('clearing the workspace'){
			steps{
				deleteDir()
			}
		}
		stage('code fetch'){
			steps{
				sh "git clone https://github.com/ansarpalakottal/ansible.git"
			}
		}
		stage('Build Artifacts'){
			steps{
				echo "Building Artifacts"
			}
		}
		stage('Checking the user'){
			steps{
				sh 'whoami'
			}
		}
		stage('Code Deploy'){
			steps{
				sh "ansible-playbook -i ansible/hosts ansible/debug.yml -vvv"
			}
		}
	}
}
