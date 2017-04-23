php7-fpm Ansible role 
=====================

This role will install php7-fpm mainly for Drupal8 Deploment

Dependencies
------------
- git@github.com:geerlingguy/ansible-role-repo-remi.git

Requirements
------------

Required packages (installed automatically) :

 - php-bcmath
 - php-cli
 - php-common
 - php-dbg
 - php-devel
 - php-fpm
 - php-gd
 - php-intl
 - php-json
 - php-mbstring
 - php-mysqlnd
 - php-opcache
 - php-pdo
 - php-pecl-apcu
 - php-pecl-apcu-bc
 - php-pecl-igbinary
 - php-pecl-memcached
 - php-pecl-mongodb
 - php-pecl-msgpack
 - php-pecl-mysql
 - php-pecl-xmldiff
 - php-pecl-xmldiff-devel
 - php-pecl-zip
 - php-process
 - php-xml
 - php-xmlrpc
 - php-runtime

Role Variables
--------------

  - `php7_memory_limit`: max memory per PHP process (default: 512M)
  - `php7_post_max_size`: max post size (default: 32M)
  - `php7_upload_max_filesize`: max upload size for files (default: 32M)

Tags
----

  - `php7-fpm` : applies to the whole role

Example Playbook
----------------

This is mainly used as a dependency in your existing playbooks, like:

    dependencies:
      - { role: ansible-php7-fpm }

but can be used in playbooks also :

    - name: web servers
      hosts: webservers
      roles:
        - ansible-php7-fpm

License
-------

MIT

Author Information
------------------

@leucos
@vorapoap

