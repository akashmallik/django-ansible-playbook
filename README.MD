# Ansible Configuration for Django Project

Ansible Configuration for Django Project (Multiple Django in single droplet)

## Getting Started

Ansible is a radically simple IT automation platform that makes your applications and systems easier to deploy and maintain.

### Prerequisites
- Python   
- Django  
- Ansible  

Installation guide for Ansible https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html  

Verify Ansible by running this cmd.
```bash
ansible --version
```

### How to run  
- Change directory to `playbooks` 
    ```shell
    cd playbooks
    ```
- Make sure you are using the correct inventory. Default inventory `inventories/local`. You can modify it from the `playbooks/ansible.cfg` file.
- Update the specified inventory variables. Variables contained in the folder you mentioned as the value of `inventory` in the `playbooks/ansible.cfg` file.
- Run `setup.yml` playbook
    ```shell
    ansible-playbook setup.yml
    ```
    ***Note:*** At the very beginning, we need to run `setup.yml` once. When this is done we will only run `sync.yml` because everything is already set up.

### Project Structure
Project structure mentioned below

``` bash
📦example
 ┣ 📂playbooks
 ┃ ┣ 📜ansible.cfg
 ┃ ┣ 📜gunicorn.service.j2
 ┃ ┣ 📜gunicorn.socket.j2
 ┃ ┣ 📜hosts
 ┃ ┣ 📜nginx.j2
 ┃ ┣ 📜setup.yml
 ┃ ┣ 📜sync.yml
 ┃ ┗ 📜vars.yml
 ┣ 📂src
 ┃ ┣ 📂project_x
 ┃ ┃ ┣ 📜asgi.py
 ┃ ┃ ┣ 📜settings.py
 ┃ ┃ ┣ 📜urls.py
 ┃ ┃ ┣ 📜wsgi.py
 ┃ ┃ ┗ 📜__init__.py
 ┃ ┣ 📂simple_app
 ┃ ┃ ┣ 📂migrations
 ┃ ┃ ┃ ┗ 📜__init__.py
 ┃ ┃ ┣ 📜admin.py
 ┃ ┃ ┣ 📜apps.py
 ┃ ┃ ┣ 📜models.py
 ┃ ┃ ┣ 📜tests.py
 ┃ ┃ ┣ 📜views.py
 ┃ ┃ ┗ 📜__init__.py
 ┃ ┗ 📜manage.py
 ┣ 📂venv
 ┃ ┣ 📂Lib
 ┃ ┣ 📂Scripts
 ┃ ┗ 📜pyvenv.cfg
 ┗ 📜requirements.txt
```

## Run in the local environment with [Vagrant](https://www.vagrantup.com/)
Requirements:  
- Vagrant
- VirtualBox (Used in this project)  

Installation guide for Vagrant https://www.vagrantup.com/downloads.  
Installation guide for VirtualBox https://www.virtualbox.org/wiki/Downloads.

After the successful installation of Vagrant and VirtualBox run the following cmd to run the local environment.
```bash
vagrant up
```
If the command runs successfully, you will be able to run the `private_network` IP (http://192.168.56.10/ for this project) specified in Vagrantfile in the browser. And it will show an Nginx page.

## Authors

* **Akash Mallik** - *Initial work* - [akashmallik](https://github.com/akashmallik)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
