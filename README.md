Ansible Role: Oracle Java Development Kit (JDK)
=========

Ansible role to install [Oracle Java Development Kit](https://www.oracle.com/java/technologies/java-se-glance.html) (JDK) on Linux Servers.

Requirements
------------

The role does not require anyting to run on RHEL and its derivatives.

Role Variables
--------------

Available variables are listed below, along with default values ```(see defaults/main.yml)```:

```
software_url: "http://www.example.org"
package_name: "jdk-11_linux-x64_bin.rpm"
```

```software_url``` **(Required)** The URL that hosts the Installer package. This should be either **http** or **https**.

```package_name``` **(Required)** The Installer package name.

Role variables can be stored with the hosts.yaml file, or in the main variables file.

Dependencies
------------

Oracle JDK is now licensed by Oracle, and requires a subscription for access to the packages.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: mikepruett3.oracle-jdk
           vars:
             software_url: "http://www.example.org"
             package_name: "jdk-11_linux-x64_bin.rpm"

License
-------

MIT

Author Information
------------------

Role created by [mikepruett3](https://github.com/mikepruett3) on [Github.com](https://github.com/mikepruett3)
