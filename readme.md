# Ansible Monorepo

<div align="center">
  <img src="tower.png" alt="tower" width="200"/>
</div>

Ansible Monorepo is a collection of my server configuration files and ansible playbooks to setup infrastructure and applications on local linux boxes.
Most of the ansible is just running docker commands.

The name ansible compose is due to most of these ansible files being a wrapper ontop of docker compose!

[Read More on my blog](https://notedwin.com)

## Folder Outline

```python
  | - rtsp - camera setup files
  | - server - ansible playbooks for main server
  ...
```

## How do I use this

I typically test changes by adding specific task to test.yml playbooks

```bash
cd server/
nvim configs/caddyfile

nvim test.yml
`
---
- name: Deploy
  hosts: test
  gather_facts: false
  become: yes
  tasks:
    - name: Get env file content
      include_vars:
        file: env.yml
        name: env

    - name: caddy
      import_tasks: tasks/caddy.yml
`

ansible-playbook -i hosts test.yml
```

After testing changes, I don't need to do anything as my dev and prod are the same :)

## Motivation

I moved my configuration from bash scripts -> ansible and docker since it seperates my applications into containers. This removes some dependency problems I was running into. Also, remvoing having to type commands into a server over SSH which gets repetive and error-prone.
