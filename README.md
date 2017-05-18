# DevOps 360° HellWorld

DevOps 360° HelloWorld is the first playbook introduction to automation with Ansible. For more details about the project, please check: http://slides.com/floriandambrine/devops360

## 0. Setup the Ansible controller

```
sudo yum install python-pip git
sudo pip install -U pip
pip install ansible==2.3.0.0
```

## 1. Write the `hello-world` automation

You should:
* Create an inventory file to interract with `ubuntu` VMs
* Use a role named `hello-world`
* Use a playbook used `hello-world.yml`
* Install `apache2` and configure a `<VirtualHost *:8080>` in `/etc/apache2/sites-available/hello-world`
    * `DocumentRoot` should be set to `/var/www/hello-world`
* Deploy an index.html file from a template that says:
```
Hello World from <hello_world_msg>
```
* Adjust the `group_vars`, `host_vars` so that `ubuntu1` `ubuntu2` and `ubuntu3` VMs display a different message.

