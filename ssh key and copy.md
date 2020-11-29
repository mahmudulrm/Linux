Create ssh-keygen.

	ssh-keygen -t rsa
	cat ~/.ssh/id_rsa.pub

Copy the key and send remote Server.

	ssh-copy-id tony@server_info

Check Pawordless ssh.
	ssh tony@server_info
