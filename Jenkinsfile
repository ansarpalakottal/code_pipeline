#!groovy
pipeline{
	agent none
	stages{
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
		stage('Push Artifacts'){
			steps{
				echo "Pushing Artifacts"
			}
		}
		stage('Code Deploy'){
			steps{
				sh "ansible-playbook -i 18.223.187.166 ansible/debug.yml"
			}
		}
		stage('clearing the workspace'){
			steps{
				deleteDir()
			}
		}
	}
}
