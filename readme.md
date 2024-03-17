# Ansible Monorepo

<div align="center">
  <img src="tower.png" alt="tower" width="200"/>
</div>

Ansible Monorepo is a collection of server configuration files, mainly ansible playbooks for a clean Debian-based server (or Laptop) with my dotfiles and applications.
It assumes you have sudo privileges and a public SSH key already setup.

## Folder Outline

```python
  | - rtsp - camera setup files
  | - server - ansible playbooks for main server (laptop as well)
  ...
```

## Motivation

I moved my configuration from bash scripts -> ansible and docker since it seperates my applications into containers. This removes some dependency problems I was running into. Also, remvoing having to type commands into a server over SSH which gets repetive and error-prone.
