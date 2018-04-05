## Requirements
	geerlingguy.java role ($ ansible-galaxy install geerlingguy.java)

## Install
	$ cd /etc/ansible/roles
	$ git clone https://github.com/alex01t/jenkins-node.git

## Example Playbook

	- hosts: jnode1
	  roles:
	    - role: geerlingguy.docker
	    - role: jenkins-node
	      jenkins_authorized_key: ssh-rsa AAA...TBZUI9 jenkins@master-jenkins.lan
	      # optional variables:
	      jenkins_username: jenkins      # default: jenkins
	      jenkins_home: /jenkins         # default: /jenkins
	      jenkins_user_groups: docker
	      # $ mkpasswd --method=sha-512
	      jenkins_password: '$6$KMDeGDJGQ...u77jH0vWecJtP/'



