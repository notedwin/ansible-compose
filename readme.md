# Ansible compose

Ansible compose is some ansible playbooks used to set up infrastructure and applications on local linux boxes.

Ansible is way better than bash scripts since it allows me automate the set up of a linux server and its dependancies without having to manually configure the server. Working directly in the terminal through SSH is fun the first couple times since i am learning new things but after a while it gets repetitive since I dont have time to burn setting up something that has been done before.

Ex.
- prod.yml runs on my biggest server, which is a repurposed consumer desktop
- rsp-cam setup a raspberry pi to be an IP camera.

The name ansible compose is due to most of these ansible files being a wrapper ontop of docker compose!