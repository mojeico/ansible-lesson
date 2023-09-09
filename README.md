# ansible-lesson

Repo with ansible 


Check ping servers    - ansible all --key-file ~/.ssh/id_rsa -i inventory -m ping -u root
Get info              - gather_facts - ansible all -m gather_facts -u root 