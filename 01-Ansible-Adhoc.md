### Ansible Ad-Hoc Lab Exercises

#### Module: reboot

**Exercise 1: Reboot all Servers**
**Objective:** Reboot all servers listed in the inventory.

**Instructions:**
1. Use the `ansible` command with the `reboot` module to reboot all servers.
2. Monitor the servers to ensure they come back online after rebooting.

**Solution:**
```bash
ansible all -m reboot
```

#### Module: copy

**Exercise 2: Copy File to Servers**
**Objective:** Copy a configuration file to all servers.

**Instructions:**
1. Use the `ansible` command with the `copy` module to copy a file to all servers.
2. Specify the source and destination paths.

**Solution:**
```bash
ansible all -m copy -a "src=/path/to/local/file dest=/path/on/server"
```

#### Module: file

**Exercise 3: Create Directory**
**Objective:** Create a directory on all servers.

**Instructions:**
1. Use the `ansible` command with the `file` module to create a directory on all servers.
2. Specify the path of the directory to create.

**Solution:**
```bash
ansible all -m file -a "path=/path/to/directory state=directory"
```

#### Module: yum

**Exercise 4: Install Package**
**Objective:** Install a package on all servers using yum.

**Instructions:**
1. Use the `ansible` command with the `yum` module to install a package on all servers.
2. Specify the package name.

**Solution:**
```bash
ansible all -m yum -a "name=<package_name> state=present"
```

#### Module: user

**Exercise 5: Create User**
**Objective:** Create a new user on all servers.

**Instructions:**
1. Use the `ansible` command with the `user` module to create a user on all servers.
2. Specify the username and other required parameters.

**Solution:**
```bash
ansible all -m user -a "name=<username> state=present"
```

#### Module: services

**Exercise 6: Start Service**
**Objective:** Start a service on all servers.

**Instructions:**
1. Use the `ansible` command with the `service` module to start a service on all servers.
2. Specify the service name.

**Solution:**
```bash
ansible all -m service -a "name=<service_name> state=started"
```

#### Module: reboot

**Exercise 7: Schedule Reboot**
**Objective:** Schedule a reboot for all servers.

**Instructions:**
1. Use the `ansible` command with the `at` module to schedule a reboot for all servers.
2. Specify the time for the reboot.

**Solution:**
```bash
ansible all -m command -a "at now+5min -f /sbin/reboot"
```

#### Module: copy

**Exercise 8: Copy Directory to Servers**
**Objective:** Copy a directory to all servers.

**Instructions:**
1. Use the `ansible` command with the `copy` module to copy a directory to all servers.
2. Specify the source and destination paths.

**Solution:**
```bash
ansible all -m copy -a "src=/path/to/local/directory dest=/path/on/server/ mode=recursive"
```

#### Module: file

**Exercise 9: Remove Directory**
**Objective:** Remove a directory from all servers.

**Instructions:**
1. Use the `ansible` command with the `file` module to remove a directory from all servers.
2. Specify the path of the directory to remove.

**Solution:**
```bash
ansible all -m file -a "path=/path/to/directory state=absent"
```

#### Module: yum

**Exercise 10: Remove Package**
**Objective:** Remove a package from all servers using yum.

**Instructions:**
1. Use the `ansible` command with the `yum` module to remove a package from all servers.
2. Specify the package name.

**Solution:**
```bash
ansible all -m yum -a "name=<package_name> state=absent"
```

These exercises cover various Ansible modules for Ad-Hoc commands and provide hands-on practice for managing servers efficiently.
