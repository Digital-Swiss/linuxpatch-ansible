# Ansible Playbook: Install and Manage linuxpatch.com Agent and Service

## Description

This Ansible playbook automates the process of downloading, executing, and cleaning up an installation script from [linuxpatch.com](https://linuxpatch.com). Additionally, it ensures that the `linuxpatch-agent` service is running and enabled at startup. The script is only executed if the file `/opt/linuxpatch/bin/linuxpatch` does not exist.

## Prerequisites

- Ansible installed on the control node.
- SSH access to the target hosts.
- Properly configured inventory file with the target hosts.
- API key for [linuxpatch.com](https://linuxpatch.com).

## Variables

- `api_key`: The API key required for the script execution. You should replace the placeholder with your actual API key.

## Usage

1. **Clone the repository or create the playbook file**:

   Save the playbook content into a file named `linuxpatch.yml`.

2. **Set up the Inventory File**:

   Ensure you have an inventory file (`hosts` or any other name) that lists the target hosts. Here is an example of an inventory file:

   ```ini
   [servers]
   server1.example.com
   server2.example.com
