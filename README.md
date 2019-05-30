# AnsibleBooks

## here is some useful details for this repository

## Ansible installation

All packages you need are given below,

Ansible,




## validation steps

Run below command
*ansible --version*


### List of modules

#### 1. ping


#### 2. shell


#### 3. yum
ansible <group> -m yum -a “name=httpd state=present” 
ansible -i inventory App1 -m yum -a "name=httpd state=present”


#### 4. service
ansible -i inventory App1 -m service -a "name=httpd state=started”

#### 5. copy
ansible -i inventory -m copy -a “src=SourceFile dest=DestFile”
