Role Name
=========

Installs Tomcat and Fedora 4 repository

Requirements
------------

Java 8 needs to be installed.

Role Variables
--------------

```yaml

fedora_version: 4.5.1

fedora_url: http://repo1.maven.org/maven2/org/fcrepo/fcrepo-webapp/{{ fedora_version }}/fcrepo-webapp-{{ fedora_version }}.war

# Directory where the Fedora war will be downloaded
install_path: /opt/install

# Directory where fedora data will persist
fedora_data_directory_path: /opt/fedora-data

# Tomcat Service Variables

tomcat_path: "/var/lib/{{ tomcat_service_name }}"
tomcat_config_path: /etc/{{ tomcat_service_name }}/Catalina/localhost

# Tomcat java opts
tomcat_permgen_memory: 128M
tomcat_min_memory: 512m
tomcat_max_memory: 4096m
```
Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible_fcrepo4

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
