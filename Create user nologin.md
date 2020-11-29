Create User nologin:

	sudo useradd -s /sbin/nologin siva   

Check: 

	cat /etc/passwd | grep nologin
	id siva 
	su siva