Ansible Role: ckan-plugins
---

This playbook is install extension of CKAN. 

Requirements
---
You need `ckan_plugins` variables for the run.

```
ckan_plugins:
  - name: "plugin-name"
    url: "path/to/repository.git"
    branch: "master"
  - name: "2nd-plugin-name"
    url: "path/to/repository.git"
    branch: "master"
```

Role Variavles
---
Avarable variables are listed below. (See defaults/main.yml)

```
url_repos: https://github,com
```
```
venv_location: /usr/lib/ckan/default
```
```
ckan_user_name: ckan
```

Dependencies
---
None

Example Playbook
---
```
- hosts: all
  roles:
    - { role: ansible-ckan-plugin }
  var:
    ckan_plugins:
      - name: "plugin-name"
        url: "path/to/repository.git"
        branch: "master"
      - name: "2nd-plugin"
        url: "path/to/repository.git"
        branch: "develop"
```


