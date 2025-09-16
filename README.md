# ansible nested become

Role for debug Ansible 12.0.0 (ansible-core 2.19) imported tasks `remote_user`
See issue [#85855](https://github.com/ansible/ansible/issues/85855)

Example playbook

```yaml
---
- name: "Ansible | Debug nested become"
  become: true
  gather_facts: true
  remote_user: <non_root_ssh_user>
  no_log: false
  strategy: linear
  roles:
    - role-for-debug
  hosts:
    - target
```
