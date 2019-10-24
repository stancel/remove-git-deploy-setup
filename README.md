remove_git_deploy_setup
=========

Ansible role that removes a git bare repository on a web server.

Requirements
------------

You'll want to already have some sort of webserver setup (Apache, NginX, etc.).

Role Variables
--------------

The file path on the server for setting up the git bare repo. The default is "/var/git".
  
```
	remove_git_deploy_setup_git_home: "/var/git"
```

List of sites to remove Git deployments for

```
	remove_git_deploy_setup_sites_to_remove:
	  - {
		  url: 'somesite.com'
		}
```

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
	- hosts: your_server
	  vars_files:
	    - vars/main.yml
	  roles:
	    - stancel.remove_git_deploy_setup
```

or just pass the variables in the playbook

```
	- hosts: your_server 
	  vars:
		remove_git_deploy_setup_sites_to_remove:
		  - {
			  url: 'somesite.com'
			}
	  roles:
	    - stancel.remove_git_deploy_setup
```

License
-------

GPLv3

Author Information
------------------

[Brad Stancel](https://github.com/stancel) 
