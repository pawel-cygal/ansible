OS: Ubuntu 14.04, Ubuntu 16.04

Example run:
```ansible-playbook -e env=test -i test setup.yml   ```

This playbook  install docker engine, without unnecessary configuration.

by default, playbook dosen't upgrades all packages in system, but we can use flag -e do_upgrade=yes to enforce apt-get upgrade
Example run:
```ansible-playbook -e env=test -i test -e do_upgrade=yes setup.yml   ```
