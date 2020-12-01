ls -ltr

#coppy file multiple servers
for instance in server-1 server-2; do
	scp testfile ${instance}:~/  //example 1
	
	// multiple line command exculpation 
	scp ca.crt ca.key kube-apiserver.key kube-apiserver.crt \
    service-account.key service-account.crt \
    etcd-server.key etcd-server.crt \
    ${instance}:~/
	
done


##multiple line command exculpation 
####example 1
{
  sudo mkdir -p /etc/etcd /var/lib/etcd
  sudo cp ca.crt etcd-server.key etcd-server.crt /etc/etcd/
}
####example 2
{
  tar -xvf etcd-v3.3.9-linux-amd64.tar.gz
  sudo mv etcd-v3.3.9-linux-amd64/etcd* /usr/local/bin/
}
####example 3
{
  sudo systemctl daemon-reload
  sudo systemctl enable etcd
  sudo systemctl start etcd
}


#cat command to create file with copy content 


:w !sudo tee  %

q!


vim ~/.vimrc
set number