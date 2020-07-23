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

#### Compulsory variables which are not set per default

###### Backend GitLab IP addresses

Specify a list of backends with name and IP address:
 
```yaml
backends:
  - backend_name: 'backend_server_1'
    backend_id: '192.168.33.10'
```

###### Frontend floating IP address

Specify the floating IP address of the frontend:

```yaml
frontend_ip: '192.168.33.100'
```

#### Compulsory variables which are set per default but need to be adapted

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

###### HAProxy logging socket path

Give the path to the HAProxy logging socket:

```yaml
haproxy_log_socket: '/dev/log'
```

###### HAProxy socket file path

Give the path to the HAProxy socket file:

```yaml
haproxy_socket: '/run/haproxy/admin.sock'
```




###### Country Name for SSL certificate

Set country to be used for the SSL certificate:

```yaml
country_name: 'DE'
```

###### State name for SSL certificate

Set state to be used for the SSL certificate:

```yaml
state_or_province_name: 'Saxony'
```

###### Locality Name for SSL certificate

Set locality to be used for the SSL certificate:

```yaml
locality_name: 'Dresden'
```

###### Organization name for SSL certificate

Set organization to be used for the SSL certificate:

```yaml
organization_name: 'Helmholtz-Zentrum Dresden-Rossendorf (HZDR)'
```

###### Organization Unit Name for SSL certificate

Set organization unit to be used for the SSL certificate:

```yaml
organizational_unit_name: 'FWCC / Computational Science'
```

###### Email address for SSL certificate

Set email address to be used for the SSL certificate:

```yaml
email_address: 'hifis-help@hzdr.de'
```

###### Common Name for SSL certificate

Set common name to be used for the SSL certificate:

```yaml
common_name: 'Helmholtz Association'
```

###### HAProxy SSL directory path

Give the path to the HAProxy SSL directory:

```yaml
haproxy_ssl_certificate_dir: '/etc/haproxy/ssl'
```

###### HAProxy Private Key file path

Give the path to the HAProxy Private Key file:

```yaml
haproxy_ssl_certificate_key_file: "/etc/haproxy/ssl/haproxy.key"
```

###### HAProxy Certificate Signing Request file path

Give the path to the HAProxy Certificate Signing Request file:

```yaml
haproxy_ssl_certificate_csr_file: '/etc/haproxy/ssl/haproxy.csr'
```

###### HAProxy Certificate file path

Give the path to the HAProxy Certificate file:

```yaml
haproxy_ssl_certificate_crt_file: "/etc/haproxy/ssl/haproxy.crt"
```

###### HAProxy PKCS12 file path

Give the path to the HAProxy PKCS12 file:

```yaml
haproxy_ssl_certificate_pkcs12_file: "/etc/haproxy/ssl/haproxy.p12"
```

###### HAProxy Certificate Chain file path

Give the path to the HAProxy Certificate Chain file:

```yaml
haproxy_ssl_certificate_chain_file: "/etc/haproxy/ssl/haproxy.pem"
```

###### HAProxy DH Parameter file path

Give the path to the DH Parameter file:

```yaml
haproxy_ssl_dhparam_file: "/etc/haproxy/ssl/dhparam.pem"
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
