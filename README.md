# Playbook-WordPress-server

Playbook-WordPress-server is an ansible playbook to install WordPress on ubuntu. This repository contains also 2 playbooks to stop or start the HTTP service

## Installation

Download directly the playbook from this Git repository

```bash
git https://github.com/MarieLePanda/Playbook-WordPress-server.git
cd Playbook-WordPress-server
```

## Configure

The file default.yml in the vars folder contains the variable to set for your WordPress installation.
It contains:

The system settings
- php_modules: All PHP modules to install

The MySQL settings
- mysql_root_password: The root password for MySQL
- mysql_db: The MySQL database to create for WordPress
- mysql_user: The MySQL user to use for WordPress
- mysql_password: The MySQL user's password

The HTTP settings
http_host: The domain name
http_conf: the name of the configuration file that will be created within Apache.
http_port: The HTTP port, default is 80.

## Run

To run the playbook
```Bash
ansible-playbook playbook.yml
```

To stop the HTTP services
```Bash
ansible-playbook manage-services/playbook-stop-apache.yml
```

To start the HTTP services
```Bash
ansible-playbook manage-services/playbook-start-apache.yml
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.



## License
[Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
