# Haas Server Deployment Playbook

## Requirements
### Local (controller) machine
- Install python3
- Install pip3
- Install ansible

## Usage
- Launch VPS (e.g. on DigitalOcen / Vultr)
- During the launch add SSH key to the instance
- This playbook uses `~/.ssh/id_rsa` to login into instance by default. You can change it in `group_vars/all` file
- Clone repo
- Create `hosts` file in the root of playbook folder with the following content:
```
[webservers]
ip_of_server1_to_configure
ip_of_server2_to_configure
```

- Put Haas' linux distribution archive (e.g. `linux32.tar.gz`) under `/roles/haas/files/`
- `$ cd path` into playbook dir
- `$ ansible-playbook -i hosts site.yml`
- Open `ip_of_server1_to_configure:8090` in the web browser

