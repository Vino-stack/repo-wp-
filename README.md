1.Terraform init,plan,apply

2.open ssh of your VM's.
    launch bash with root privilege
    sudo sh install.sh
    
3.Authorize VM'S IP on cloud SQL
  cloud sql->connections->authorization -> set CIDR range(External IP of VM) 
  
5.Configuring your Cloud SQL instance for WordPress

    mysql -h SQL_INSTANCE_IP -u root -p

    CREATE DATABASE wordpress;

    CREATE USER wordpress IDENTIFIED BY 'very-long-wordpress-password';

    GRANT ALL PRIVILEGES ON wordpress.* TO wordpress;

    FLUSH PRIVILEGES;
    
4.Open a browser and enter your server’s IP or virtual domain name on URL using the HTTP protocol.
  http://your_server_IP/index.php








Reference:
https://livebook.manning.com/book/google-cloud-platform-in-action/chapter-2/1


https://www.tecmint.com/install-wordpress-using-apache-in-debian-ubuntu-linux-mint/



https://binx.io/blog/2018/11/19/how-to-configure-global-load-balancing-with-google-cloud-platform/
