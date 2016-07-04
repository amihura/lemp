## WordPress+phpMyAdmin+Nginx+PHP-FPM(Apache)+proftpd

To run the playbook:
- Edit the `hosts` inventory file to include the names or URLs of the servers
you want to deploy.
- Set proper hostname in `group_vars/all` server_hostname: www.arturmihura.tk

Run the playbook using:

    ansible-playbook -i hosts site.yml --ask-vault-pass


If you want to use Apache instead of PHP-FPM run playbok:

    ansible-playbook -i hosts site.yml --extra-vars "php_handler="apache" --ask-vault-pass

By defaul this value is set to php_handler="php-fpm" in `group_vars/all`



