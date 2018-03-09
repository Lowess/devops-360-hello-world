# DevOps 360° Hello-World

DevOps 360° Hello-World is the first playbook introduction to automation with Ansible. For more details about the project, please check: http://slides.com/floriandambrine/devops360

## 0. Setup the Ansible controller

```
sudo yum install python-pip python-devel gcc git
sudo pip install -U pip
pip install ansible==2.4.3.0
```

## 1. Write the `hello-world` automation

__You should:__
* Create an inventory file to interract with `ubuntu` VMs
* Use a role named `hello-world`
* Use a playbook named `hello-world.yml`
* Install `nginx` and configure a `server block` in `/etc/nginx/sites-available/hello-world` (This resource can be useful: [How To Set Up nginx Virtual Hosts ](https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-virtual-hosts-server-blocks-on-ubuntu-12-04-lts--3))
* `root` should be set to `/opt/hello-world`
* Deploy an index.html file in `/opt/hello-world` from a template that says:
```
Hello <hello_world_msg>!
```
* `hello_world_msg` should default to `World`
* Adjust the `group_vars`, `host_vars` so that `ubuntu1` `ubuntu2` and `ubuntu3` VMs display a different message.
