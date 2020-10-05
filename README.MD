# Ansible Configuration for Django Project

Ansible Configuration for Django Project (Multiple Django in single droplet)

## Getting Started

Ansible is a radically simple IT automation platform that makes your applications and systems easier to deploy and maintain.

### Prerequisites

Install Ansible first

```
pip install ansible
```

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
 ┃ ┃ ┣ 📂__pycache__
 ┃ ┃ ┃ ┣ 📜settings.cpython-37.pyc
 ┃ ┃ ┃ ┗ 📜__init__.cpython-37.pyc
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

## Authors

* **Akash Mallik** - *Initial work* - [akashmallik](https://github.com/akashmallik)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
