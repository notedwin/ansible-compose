# Ansible Monorepo

<div align="center">
  <img src="tower.png" alt="tower" width="200"/>
</div>

Ansible Monorepo is a collection of server configuration files for my homelab.
Devices included:

- SFF PC (main server)
- OpenWRT Router
- Raspberry Pi as a camera
- Laptop

All devices are running Debian-based OS and assumed to have sudo privileges and a public SSH key already setup.

## Rules

Do not configure anything manually. Use Ansible to automate the process.
Do not install anything on the host machine. Use Docker to run applications.

## Folder Outline

```python
  | - rtsp - camera setup files
  | - server - ansible playbooks for main server (laptop as well)
  ...
```

## Motivation

I moved my configuration from bash scripts -> ansible and docker since it seperates my applications into containers. This removes some dependency problems I was running into. Also, remvoing having to type commands into a server over SSH which gets repetive and error-prone.
