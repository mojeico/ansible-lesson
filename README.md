# ansible-lesson

Repo with ansible 


Check ping servers    	- ansible all --key-file ~/.ssh/id_rsa -i inventory -m ping -u root
Get info              	- ansible all -m gather_facts -u root 
Install vim-box by apt  - ansible all -m apt -a name=vim-nox
Run  ansible playbook 	- ansible-playbook install_httpd.yml


