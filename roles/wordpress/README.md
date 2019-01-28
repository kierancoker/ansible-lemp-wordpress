Role Name
=========

This role installs and configures a wordpress instance on either a RHEL or Debian platform

Requirements
------------

You will need PHP, NGINX/Apache and MariaDB/MySQL installed on your server

Role Variables
--------------

wp_cli:
  download: -> link to the wordpress phar file
  path: -> where to download too

wp_database:
  name: => database name
  username: -> database username
  password: -> database password

wordpress:
  domain: -> desired domain reference
  title: -> Title of the wordpress page
  username: -> wordpress username
  password: -> wordpress password to login to the admin
  email: -> email address for the above user
  theme: -> theme for the website
  plugins: -> any third-party plugins


Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - roles/wordpress

License
-------

BSD
