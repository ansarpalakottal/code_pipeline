#!groovy
pipeline{
	agent any
	stages{
		stage('code fetch'){
			steps{
				sh "git clone https://github.com/ansarpalakottal/ansible.git"
			}
		}
		stage('Checkout to playbook folder'){
			steps{
				sh "cd ansible"
			}
		}
		stage('checking working directory'){
			steps{
				sh "pwd"
			}
		}
		stage('Code Deploy'){
			steps{
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
