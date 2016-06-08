Role Name
=========

Install ReviewBoard on RedHat / CentOS 7, Debian Jessie, or Gentoo

Requirements
------------

When hiawatha or lighttpd is selected as web server, the packages needed to run it with fcgi support should be installed ahead of time. This role does not currently install those packages. Note that hiawatha is not available in official repos for RedHat or Debian.

Role Variables
--------------

* reviewboard_version
* reviewboard_topdir
* reviewboard_appdir
* reviewboard_staticdir
* admin_user
* admin_password
* admin_email
* repo_group
* sql_database_type
* sql_database_name
* sql_database_host
* sql_username
* sql_password
* web_cache_type
* web_cache_info
* app_server_type
* web_server_type
* web_server_hostname
* web_server_ip
* web_server_port
* firewall_type

Dependencies
------------

No other dependencies.


Example Playbook
----------------

Example playbook

    - hosts: servers
      remote_user: root
      roles:
         - { role: reviewboard, sql_username: reviewboard, sql_password: password, sql_database_name: reviewboard, sql_database_host: localhost, reviewboard_version: 3.2.1, app_server_type: uwsgi, web_server_type: uwsgi, firewall_type: firewalld }

License
-------

BSD

Author Information
------------------

S. Lockwood-Childs
based on bngsudheer.reviewboard role by Sudheer Satyanarayana
