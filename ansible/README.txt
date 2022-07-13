yaml 

setting up environment
	- you can use virtual machines or real machines or use cloud providers machines or mix of all of these. connection between acn and node is enough
	- ansible control node with ansible python and ssh-client installed (optionally sshpass)
	- other nodes with sshd and python installed
	- (optionally) edit /etc/hosts file for name resolution if servers does not have 
	- make initial connections with nodes from acn (fow known hosts file) (you may want to add '[defaults]\n host_key_checking = False' to ansible.cfg file for not making initial connections but this is not recommended)
	- create ssh key and(you can use ssh-agent for passphrase or do not use passphrase for connections)
		- copy key files manually (ssh-copy-id)
		- copy key files automated (ansible --ask-pass) (install sshpass)
			- make sure authorized_keys file exists
			- ansible --ask-pass -i hosts.ini -m ansible.builtin.file -a "path=/home/ubuntu/.ssh/authorized_keys owner=ubuntu group=ubuntu mode='0600'" all
			- append your private-key to authorized_keys file
			- ansible --ask-pass -i hosts.ini -m ansible.builtin.shell -a "echo [public key file conents] >> /home/ubuntu/.ssh/authorized_keys" all
			- verify your key is there
			- ansible --ask-pass -i hosts.ini -m ansible.builtin.shell -a "cat /home/ubuntu/.ssh/authorized_keys" all
			- then connect with key
			- ansible -i hosts.ini -m ping (--private-key or --key-file) [private key file] all (or use ansible_ssh_private_key_file var in inventory and do not specify key file in command)
	- before configure sshd learn become and ask-become-pass privilege-escalation
	- configure sshd to (create a sshd_config file then copy or learn regex in ansible.builtin.replace examples)(after following steps you wont be able to ssh directly to the machines you control if ansible control node is not machine you are using. you could create one more ssh key for your machine too if you want to ssh directly)
		- Not permit root login
		- accept publickey authentication
		- do not accept password authentication
	- restart sshd service (service module)
	- make sure acn can ping nodes

ansible.cfg
inventory
fork -f


real world scenario
