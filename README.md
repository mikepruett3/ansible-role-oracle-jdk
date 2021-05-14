Ansible Role: Oracle Java Development Kit (JDK)
=========

Ansible role to install [Oracle Java Development Kit](https://www.oracle.com/java/technologies/java-se-glance.html) (JDK) on Linux Servers.

Requirements
------------

The role does not require anyting to run on RHEL and its derivatives. This role assumes that you have the software package located on a web server somewhere in your environment.

Role Variables
--------------

Available variables are listed below, along with default values ```(see defaults/main.yml)```:

``` yaml
software_url: "http://www.example.org"
package_name: "jdk-11_linux-x64_bin.rpm"
java_version: "11"
```

```software_url``` **(Required)** The URL that hosts the Installer package. This should be either **http** or **https**.

```package_name``` **(Required)** The Installer package name.

```java_version``` **(Required)** The version of Oracle Java Development Kit that is to be installed.

Role variables can be stored with the hosts.yaml file, or in the main variables file.

Dependencies
------------

Oracle JDK is now licensed by Oracle, and requires a subscription for access to the packages.

Example Playbook
----------------

``` yaml
    - hosts: servers
      roles:
         - role: mikepruett3.oracle-jdk
           vars:
             software_url: "http://www.example.org"
             package_name: "jdk-11_linux-x64_bin.rpm"
             java_version: "11"
```

License
-------

MIT

Author Information
------------------

Role created by [mikepruett3](https://github.com/mikepruett3) on [Github.com](https://github.com/mikepruett3)
