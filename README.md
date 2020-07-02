<!--
SPDX-FileCopyrightText: 2020 Helmholtz Centre for Environmental Research (UFZ)
SPDX-FileCopyrightText: 2020 Helmholtz-Zentrum Dresden-Rossendorf (HZDR)

SPDX-License-Identifier: Apache-2.0
-->

HAProxy Role
============

Role sets up a HAProxy instance to be used as a load balancer in a
High Availability and Scalability context.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

#### Compulsory Variables to be Changed for the Configuration File

###### Number of processors used by HAProxy

Sets number of processors used by HAProxy:

```yaml
haproxy_nbproc: '1'
```

###### Number of threads used by HAProxy

Sets number of threads used by HAProxy:

```yaml
haproxy_nbthread: '2'
```

###### HAProxy CPU Map for Multithreading

Mapping threads to CPU cores:

```yaml
haproxy_cpumap: 'auto:1/1-2 0-1'
```

###### Backend GitLab IP addresses

Specify a list of backends with name and IP address:
 
```yaml
backends:
  - backend_name: 'gitlab_server_1'
    backend_id: '192.168.33.10'
```

###### Frontend floating IP address

Specify the floating IP address of the frontend:

```yaml
frontend_ip: '192.168.33.100'
```

###### HAProxy Certificate Data for the Self-Signed SSL Certificate

For a Self-Signed SSL Certificate you need at least these data:

```yaml
haproxy_self_signed_certificate_data: "/C=DE/ST=Saxony/L=Dresden/O=Helmholtz-Zentrum Dresden-Rossendorf (HZDR)/CN=haproxy"
```

###### Enable/disable stats

Variable to enable or disable the stats:

```yaml
stats_enable: 'enable'
```

###### Stats admin user name

Variable to hold the stats admin user name:

```yaml
stats_admin_user: 'admin'
```

###### Stats admin user password

Variable to hold the stats admin user password:

```yaml
stats_admin_user_password: 'changeme'
```

#### All other Default Variables

###### HAProxy PPA version

Variable to pin the PPA version to a certain value:

```yaml
haproxy_ppa_version: 'ppa:vbernat/haproxy-2.1'
```

###### HAProxy version

Variable to pin the HAProxy version to a certain value:

```yaml
haproxy_version: '2.1.*'
```

###### HAProxy user

Variable to specify the HAProxy system user:

```yaml
haproxy_user: 'haproxy'
```

###### HAProxy group

Variable to specify the HAProxy system group:

```yaml
haproxy_group: 'haproxy'
```

###### HAProxy HAProxy dependencies to be installed

List of HAProxy dependencies to be installed:

```yaml
haproxy_dependencies:
  - 'software-properties-common'
```

###### HAProxy binary name

Name of the HAProxy binary:

```yaml
haproxy_name: 'haproxy'
```

###### HAProxy configuration directory path

Give the path to the HAProxy configuration directory:

```yaml
haproxy_conf_dir: '/etc/haproxy/'
```

###### HAProxy configuration file path

Give the path to the HAProxy configuration file:

```yaml
haproxy_conf_file_path: "/etc/haproxy/haproxy.cfg"
```

###### HAProxy logging directory path

Give the path to the HAProxy logging directory:

```yaml
haproxy_log: '/var/log/haproxy/'
```

###### HAProxy socket file path

Give the path to the HAProxy socket file:

```yaml
haproxy_socket: '/run/haproxy/admin.sock'
```

###### HAProxy SSL directory path

Give the path to the HAProxy SSL directory:

```yaml
haproxy_ssl_certificate_dir: '/etc/haproxy/ssl'
```

###### HAProxy Certificate file path

Give the path to the HAProxy certificate file:

```yaml
haproxy_ssl_certificate_key_file: "/etc/haproxy/ssl/haproxy.crt"
```

###### HAProxy Private Key file path

Give the path to the HAProxy private key file:

```yaml
haproxy_ssl_certificate_cert_file: "/etc/haproxy/ssl/haproxy.key"
```

###### HAProxy combined Certificate and Private Key file path

Give the path to the combined Certificate and Private Key file:

```yaml
haproxy_ssl_certificate_cert_file_combined: "/etc/haproxy/ssl/haproxy.pem"
```

###### HAProxy dhparam file path

Give the path to the dhparam file:

```yaml
haproxy_ssl_certificate_dhparam_file: "/etc/haproxy/ssl/dhparam.pem"
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

[Apache-2.0](LICENSES/Apache-2.0.txt)

Author Information
------------------

HIFIS Software Team (please visit [HIFIS Software Webpage](https://software.hifis.net))
