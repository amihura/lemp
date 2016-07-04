## WordPress+phpMyAdmin+Nginx+PHP-FPM(Apache)+vsftpd

To run the playbook:
Edit the `hosts` inventory file to include the names or URLs of the servers
you want to deploy.

Run the playbook using:

    ansible-playbook -i hosts site.yml


If you want to use Apache instead of PHP-FPM run playbok:

    ansible-playbook -i hosts site.yml --extra-vars "php_handler="apache"

By defaul this value is set to php_handler="php-fpm" in `group_vars/all`



