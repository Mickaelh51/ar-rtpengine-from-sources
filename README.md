# Ansible role for RTPEngine (Compilation from sources)

Ansible role for RTPEngine (https://www.sipwise.com/)

## Tasks
- Choose RTPEngine version {{ rtpengine_version }}
- Install dependencies packages
- Create RTPEngine User and Group
- Clone RTPEngine repository from GitHub
- Compile from sources
- Install from sources
- add IPtables kernel support
- Add default, systemd, ... files


## Requirements
- Tested with vagrant box (Debian 8 / 9)
- Ansible 2.7.4

## Start to play
```
service ngcp-rtpengine-daemon start
```

## Ansible Galaxy
https://galaxy.ansible.com/***********
```
ansible-galaxy install mickaelh51.**********
```

## Enhancements
- Add CentOS 6 / 7 support
- Replace root by rtpengine user and group to start it
