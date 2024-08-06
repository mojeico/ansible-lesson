# ansible-lesson




- Generate key -> ssh-keygen -t ed25519 -C "my ssh"

- vim .ssh/authorized_keys - add pub key 

ssh 165.22.121.23 -i /Users/glebmojeico/.ssh/do

chmod 600 /Users/glebmojeico/.ssh/do

ssh root@165.22.121.23 -i /Users/glebmojeico/.ssh/do



Repo with ansible 


!!!!!!!!  --check - dry-run !!!!!!!!!!

- Check ping servers    	    - ansible all -m ping -i inventory -u g_mojeico --key-file ~/.ssh/id_ed25519
- Get info              	    - ansible all -m gather_facts -u root 
- Install                       - ansible all -m apt -a name=snapd  -u root





playbook: ubuntu.yml

  play #1 (ubuntu): ubuntu	TAGS: []
      TASK TAGS: [debug, install, ubuntu]




- Run playbook                            - ansible-playbook install_apache.yml -u root
- Dry run                                 - ansible-playbook install_apache.yml -u root --check
- Run playbook only with "web-server" tag -  ansible-playbook --tags web-server  install_apache.yml -u root      -  add in task tags: web-server
