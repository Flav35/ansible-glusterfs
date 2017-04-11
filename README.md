Role
====
GlusterFS - Install package, setup cluster and create volumes

Requirements
------------
- ansible 2.1
- Hosts in a ``glusterfs`` inventory group

Role Vars
---------
### 
```yaml
    glusterfs_brick_dir: "/data/brick"
    glusterfs_volumes:
        - config
```
Dependencies
------------
None


Playbook examples
-----------------

```yaml
    - hosts: glusterfs
      roles:
        - ansible-glusterfs
```

```yaml
    - hosts: glusterfs
      roles:
        - role: ansible-docker-install
          glusterfs_volumes:
            - config
            - data
          glusterfs_bricks_dir: "/srv/data/"
```

Distrib Support
---------------
| Distribution | Compat | Test  |
| ------------ |:------:|:-----:|
|    CentOS 7  |   N    |   N   |
| Ubuntu 16.04 |   Y    |   Y   |


TODO
----
* CentOS 7 compat
