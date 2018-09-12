#!groovy
pipeline{
	agent any
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
				sh "cd ansible"
				sh "ansible-playbook -i localhost debug.yml"
			}
		}
		stage('clearing the workspace'){
			steps{
				deleteDir()
			}
		}
	}
}
