# ansible-role-radarr
 
=========

Ansible Role to install radaar, an automated downloader, watchlist, monitoring program for movies.

Requirements
------------

Minimum Ansible version required is Ansible 2.9

Role Variables
--------------
Role variables have good defined defaults, which are located in `defaults/main.yml`.
Current version includes the following variables with default values:

### Defaults
| Name               | Default Value | Description                  |
|--------------------|---------------|------------------------------|
| `radarr_user`       | radarr | The primary user to run radarr     |
| `radarr_uid`        | *optional* | Commented out by default |
| `radarr_group`      | media | The primary group for `radarr_user` |
| `radarr_group_gid`  | *optional* | Commented out by default |
| `radarr_base_install_dir` | /opt/radarr | Install directory for radarr |
| `radarr_config_dir` |  /opt/data/radarr | Data directory to store configuration |
| `radarr_download_url` | https://radarr.servarr.com/v1/update/master/updatefile?os=linux&runtime=netcore&arch=x64| Link to the radarr git hub latest release |
| `radarr_port` | 7878 | Port in which radarr operates on, to add to Firewalld |
| `radarr_packages` |   `- curl` `- sqlite` | List of Packages Required to install and run radarr |

Dependencies
------------

None

Example Playbook
----------------

   - hosts: radarr_servers
      roles:
        - aaron_cole.ansible_role_radarr


License
-------

GPLv3

Author Information
------------------

Created by Aaron Cole

