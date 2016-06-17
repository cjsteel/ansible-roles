# Ansible Role: Kernel

This role will assume the setup of kernel

It's part of the Manala <a href="http://www.manala.io" target="_blank">Ansible stack</a> but can be used as a stand alone component.

## Requirements

None.

## Dependencies

None.

## Installation

### Ansible 2+

Using ansible galaxy cli:

```bash
ansible-galaxy install manala.kernel
```

Using ansible galaxy requirements file:

```yaml
- src: manala.kernel
```

## Role Handlers

None

## Role Variables

| Name                       | Default | Type  | Description                              |
| -------------------------- | ------- | ----- | ---------------------------------------- |
| `manala_kernel_modules`    | []      | Array | Kernel modules to enable/disable         |
| `manala_kernel_parameters` | []      | Array | Kernel parameters to configure           |

### Configuration example

```yaml
manala_kernel_parameters:
  - name: net.ipv4.ip_nonlocal_bind
    value: 1

manala_kernel_modules:
  - ip_vs
```

## Example playbook

```yaml
- hosts: servers
  roles:
    - { role: manala.kernel }
```

# Licence

MIT

# Author information

Manala [**(http://www.manala.io/)**](http://www.manala.io)
