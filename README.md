Percona Ansible Role
====================
[![Build Status](https://travis-ci.org/MetaRed/percona_ansible_role.svg?branch=master)](https://travis-ci.org/MetaRed/percona_ansible_role)
[![License: Apache](https://img.shields.io/badge/License-Apache_2.0-red.svg)](http://www.apache.org/licenses/LICENSE-2.0)
[![Ansible Role: version](https://img.shields.io/badge/Ansible Role-v0.0.1-blue.svg)](https://github.com/MetaRed/percona_ansible_role/releases/tag/v0.0.1)


Ansible role installs percona server, percona client, and percona toolkit.

#### Requirements: `None`
#### Dependencies: `None`

Role Variables
--------------

<table>
  <tr>
    <th>Variable</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>{{ percona_version }}</tt></td>
    <td>percona server version</td>
    <td><tt>5.5</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_data_dir }}</tt></td>

    <td>database data directory</td>
    <td><tt>/data/mysql</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_bin_log_dir }}</tt></td>

    <td>binary log directory</td>
    <td><tt>/log/data/mysql</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_bin_log }}</tt></td>

    <td>binary log file</td>
    <td><tt>mysql-bin</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_relay_log }}</tt></td>

    <td>relay log file</td>
    <td><tt>mysql-relay-log</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_log_dir }}</tt></td>

    <td>info log directory</td>
    <td><tt>/var/log/mysql</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_error_log }}</tt></td>

    <td>error log file</td>
    <td><tt>mysql-error.log</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_slow_log }}</tt></td>

    <td>slow log file</td>
    <td><tt>mysql-slow.log</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_innodb_buffer_pool_size }}</tt></td>
    <td>innodb buffer pool size</td>
    <td><tt>1G</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_mysql_read_only }}</tt></td>

    <td>slave read only mode</td>
    <td><tt>FALSE</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_server_sync_binlog }}</tt></td>
    <td>whether to sync binary logs</td>
    <td><tt>1</tt></td>
  </tr>
  <tr>
    <td><tt>{{ percona_mysql_server_id }}</tt></td>
    <td>unique db identifier</td>
    <td><tt>1</tt></td>
  </tr>
</table>

Galaxy Playbook Usage
---------------------

```yaml
    - hosts: servers
      roles:
         - { role: MetaRed.percona, variable: value }
```
Testing
-------
`ServerSpec`:
```
test/integration/percona_server
```

Authors
-------

Authors: Richard Lopez
