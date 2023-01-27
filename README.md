# pmm-agent-setup  
**Step-1 :** Login your server using ssh  
`$ ssh host_name`  
**Step-2 :** Configure repositories  
`$ wget https://repo.percona.com/apt/percona-release_latest.generic_all.deb`   
`$ dpkg -i percona-release_latest.generic_all.deb`  
**Step-3 :** Install the PMM Client package  
`$ sudo apt update`  
`$ sudo apt install -y pmm2-client`  
**Step-4 :** Check pmm2-client installed or not  
`$ pmm-admin --version`  
**Step-5 :** Register your client node with PMM Server  
`$ pmm-admin config --server-insecure-tls --server-url=https://grafana_usr_name:grafana_usr_pass@monitoring_server_private_ip`  
**Example** `$ pmm-admin config --server-insecure-tls --server-url=https://admin:abc@X.X.X.X`  

