# AWS-instance-monitoring

# Installing Nagios on ubuntu VM using
- sudo apt-get update
- sudo apt-get install -y autoconf gcc libc6 make wget unzip apache2 php libapache2-mod-php7.4 libgd-dev
- sudo apt-get install openssl libssl-dev

![image](https://github.com/user-attachments/assets/543a66e0-b598-4a19-b181-15ebcc99ce45)

 
# Downloading the Source
- cd /tmp
- wget -O nagioscore.tar.gz https://github.com/NagiosEnterprises/nagioscore/archive/nagios-4.4.14.tar.gz
- tar xzf nagioscore.tar.gz

![image](https://github.com/user-attachments/assets/330c1b27-ec21-492f-bdca-329b66ab8a99)


# Compile
- cd /tmp/nagioscore-nagios-4.4.14/
- sudo ./configure --with-httpd-conf=/etc/apache2/sites-enabled
- sudo make all

![image](https://github.com/user-attachments/assets/a090ab52-7824-46a3-8f61-0ffdea15bbf1)
![image](https://github.com/user-attachments/assets/f1374933-8e91-451a-a2ac-330c99cb1059)


# Create User And Group This creates the nagios user and group. The www-data user is also added to the nagios group.

- sudo make install-groups-users
- sudo usermod -a -G nagios www-data

![image](https://github.com/user-attachments/assets/c2954fcb-d599-44b9-a695-8b2590b0e0d8)


# Install Binaries This step installs the binary files, CGIs, and HTML files.

- sudo make install
![image](https://github.com/user-attachments/assets/e861f6e7-35a3-4e9c-bf20-9c4997bc0c3c)
 

# Install Service / Daemon This installs the service or daemon files and also configures them to start on boot.

- sudo make install-daemoninit
 
# Install Command Mode This installs and configures the external command file.

- sudo make install-commandmode

# Install Configuration Files This installs the *SAMPLE* configuration files. These are required as Nagios needs some configuration files to allow it to start.

- sudo make install-config

![image](https://github.com/user-attachments/assets/2db02e00-8243-454d-b6c9-e26f34bdd7b2)

 
# Install Apache Config Files This installs the Apache web server configuration files and configures Apache settings.

- sudo make install-webconf
- sudo a2enmod rewrite
- sudo a2enmod cgi

![image](https://github.com/user-attachments/assets/500bf97e-517d-4e6d-b4f5-7f8cd2233594)

 

# Configure Firewall You need to allow port 80 inbound traffic on the local firewall so you can reach the Nagios Core web interface.

- sudo ufw allow Apache
- sudo ufw reload

![image](https://github.com/user-attachments/assets/7842501d-5d05-40ae-ab69-ab117ae8f4c3)

 

# Create nagiosadmin User Account
- sudo htpasswd -c /usr/local/nagios/etc/htpasswd.users nagiosadmin

![image](https://github.com/user-attachments/assets/7bb20fc8-007d-4169-a933-94d1fd6ffbbf)



# Start Apache Web Server
- sudo systemctl restart apache2.service

# Start Service / Daemon
- sudo systemctl start nagios.service

![image](https://github.com/user-attachments/assets/ee253966-9a5f-456f-be83-1a7fd9dd8393)



![image](https://github.com/user-attachments/assets/db8fb042-2f8b-4394-8180-24a70e959865)

![image](https://github.com/user-attachments/assets/11be50af-1002-46d6-922a-b22d86edc58d)


# Prerequisites Make sure that you have the following packages installed.

- sudo apt-get install -y autoconf gcc libc6 libmcrypt-dev make libssl-dev wget bc gawk dc build-essential snmp libnet-snmp-perl gettext
 

# Downloading The Source
- cd /tmp
- wget --no-check-certificate -O nagios-plugins.tar.gz https://github.com/nagios-plugins/nagios-plugins/archive/release-2.4.6.tar.gz
- tar zxf nagios-plugins.tar.gz
 

# Compile + Install
- cd /tmp/nagios-plugins-release-2.4.6/
- sudo ./tools/setup
- sudo ./configure
- sudo make
- sudo make install

![image](https://github.com/user-attachments/assets/476d952a-576b-4774-9bb0-d3f06354ac7c)

![image](https://github.com/user-attachments/assets/a6a22190-8918-424d-adad-4c3aa1a775e7)

![image](https://github.com/user-attachments/assets/ba1a8e63-441e-4f03-b00c-600ee8676ecb)

![image](https://github.com/user-attachments/assets/3e38d7c9-ae39-48c8-8cfa-79077d305950)

![image](https://github.com/user-attachments/assets/736eaa53-d374-4270-9971-6e582260fb8d)



Now Let's begin the Project Journey !

![image](https://github.com/user-attachments/assets/417f4919-42b9-4500-8a0e-5e4b104f2925)



