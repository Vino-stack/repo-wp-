1.Terraform init,plan,apply

2.Authorize VM'S IP on cloud SQL
  cloud sql->connections->Authorized networks -> set CIDR range(External IP of VM) 
  
3.open ssh of your VM's.
    launch bash with root privilege
    sudo sh install.sh
  
4.Clone source code repo
    git clone https://github.com/Vino-stack/repo-wp-.git
    sudo sh install.sh
    
5.Configuring your Cloud SQL instance for WordPress

    sudo mysql -h SQL_INSTANCE_IP -u root -p

    CREATE DATABASE wordpress;

    CREATE USER wordpress IDENTIFIED BY 'very-long-wordpress-password';

    GRANT ALL PRIVILEGES ON wordpress.* TO wordpress;

    FLUSH PRIVILEGES;
    
6.Open a browser and enter your server’s IP or virtual domain name on URL using the HTTP protocol,
  to verify your wordpress deployment
  http://your_server_IP/index.php
