<!-- This was created with Claude Code -->

# Website Automation

[![Contribute](https://img.shields.io/badge/OpenShift-Dev%20Spaces-525C86?logo=redhatopenshift&labelColor=EE0000)](https://devspaces.apps.ocp.shadowman.dev/#https://github.com/shadowman-lab/Ansible-Website)


This directory contains Ansible automation for website management and operations.

## Overview

The Website automation provides playbooks and roles for managing and configuring
website infrastructure and services.

## Roles

| Role | Description |
| ---- | ----------- |
| [deploy_default_apache_conf](roles/deploy_default_apache_conf/README.md) | Role for deploy default apache conf |
| [deploy_new_release](roles/deploy_new_release/README.md) | Role for deploy new release |
| [hashi_pki_certificate](roles/hashi_pki_certificate/README.md) | Role for hashi pki certificate |
| [httpd_status](roles/httpd_status/README.md) | Role for httpd status |
| [new_release](roles/new_release/README.md) | Role for new release |
| [start_services](roles/start_services/README.md) | Role for start services |
| [stop_services](roles/stop_services/README.md) | Role for stop services |
| [verification_collection](roles/verification_collection/README.md) | Role for verification collection |
| [webservers_certificate](roles/webservers_certificate/README.md) | Role for webservers certificate |
| [webservers_collection](roles/webservers_collection/README.md) | Role for webservers collection |

## Playbooks

| Playbook | Description | Target Hosts |
| -------- | ----------- | ------------ |
| Gitea Deploy New Release.yml | Playbook for Gitea Deploy New Release | {{ vm_name | default('all') }} |
| Gitea New Release.yml | Playbook for Gitea New Release | localhost |
| Restore Default Apache Service.yml | Playbook for Restore Default Apache Service | {{ vm_name | default('all') }} |
| Start Services.yml | Playbook for Start Services | all |
| Stop Services.yml | Playbook for Stop Services | all |
| Web Certificate Hashi.yml | Playbook for Web Certificate Hashi | {{ vm_name | default('all') }} |
| Web Certificate Rotation.yml | Playbook for Web Certificate Rotation | {{ vm_name | default('all') }} |
| Web Install and Verification collections.yml | Playbook for Web Install and Verification collections | {{ vm_name | default('all') }} |
| Web Status.yml | Playbook for Web Status | {{ vm_name | default('all') }} |
| Web Verification collections.yml | Playbook for Web Verification collections | {{ vm_name | default('all') }} |

## Usage

### Running with ansible-navigator

```bash
# Run a playbook
ansible-navigator run Gitea Deploy New Release.yml

# Run in stdout mode
ansible-navigator run Gitea Deploy New Release.yml -m stdout
```

### Using roles

```yaml
- hosts: target_hosts
  roles:
    - deploy_new_release
```

## Requirements

- Ansible 2.9 or higher (via ansible-navigator)
- Required collections (see `collections/requirements.yml` if present)
- Appropriate access credentials configured via environment variables

## Directory Structure

```
Ansible-Website/
├── roles/              # Ansible roles
├── *.yml               # Playbooks
├── collections/        # Collection dependencies (if present)
└── ansible-navigator.yml  # Navigator configuration
```
