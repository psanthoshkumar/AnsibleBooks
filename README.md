# AnsibleBooks

## here is some useful details for this repository


## step 0
recommended to have dedicated ansible user on Prod client servers

if *adminansible* is the unix local ID, add following line in sudoer file

	adminansible	ALL=NOPASSWD:	ALL

## Ansible installation

All packages you need are given below,

Ansible,

## general ansible commands
	check version	=>	ansible --version
	to check list of ansible modules	=>	ansible-doc -l
	to chck details of one modules 	=>	ansbile-doc -s moduleName

	



## validation steps

Run below command
*ansible --version*


### List of modules

#### 1. ping


#### 2. shell
ansible -i inventory App1 -m shell -a "uname -a; df -Th"

#### 3. yum
ansible <group> -m yum -a “name=httpd state=present” 
ansible -i inventory App1 -m yum -a "name=httpd state=present”


#### 4. service
ansible -i inventory App1 -m service -a "name=httpd state=started”

#### 5. copy
ansible -i inventory -m copy -a “src=SourceFile dest=DestFile”



## Ansible Roles:
Roles in ansible are next level abstration of ansible playbooks

##### advantages:
- idea of include files and combine them to form clean, reusable abstraction
- Easy to maintain and troubleshoot the playbooks

##### Structure of Roles:

	<fieldset>
	contains regular files those need to be copied to target systems


	</fieldset>


	files:		contains regular files those need to be copied to target systems
	handlers :		event handlers
	meta :		role dependencies
	templates :		similar to files, but, it contains dynamic data
	tasks :		playbook tasks
	vars/group_vars :		variables definitions
