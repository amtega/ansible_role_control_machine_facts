# Ansible control_machine_facts role

This is an [Ansible](http://www.ansible.com) role that setup facts about ansible control machine host. It can be very useful in tower environments to discover the hostname of the ansible control machine and launch tasks on it using ssh, as in tower localhost tasks are forbidden by default.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

The role setups the following facts:

-  `control_machine_hostname` hostname of the control machine.

## Example Playbook

This is an example playbook:

```yaml
---

- hosts: localhost
  roles:
    - role: amtega.control_machine_facts
      vars:
        control_machine_group: myansiblegroup
```

## Testing

Tests are based on [molecule with docker containers](https://molecule.readthedocs.io/en/latest/installation.html).

```shell
cd amtega.control_machine_facts

molecule test --all
```

## License

Copyright (C) 2020 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Juan Antonio Valiño García.
