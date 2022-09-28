# Ansible Role: Budibase

Runs a [Budibase](https://budibase.com) docker container on a Linux host. Budibase is a low-code platform for creating internal apps, workflows, and admin panels.

## Requirements

Budibase is distributed as a container image on DockerHub and therefore requires that Docker be installed. 

  - Docker (Recommended: `geerlingguy.docker`)
  - General Ansible Collection (`ansible-galaxy collection install community.general`)

## Role Variables

Available variables are described below, along with default values (see `defaults/main.yml`):


## Example Playbook

The playbook below .

    - hosts: webserver
      vars_files:
        - vars/main.yml
      roles:
        - geerlingguy.docker
        - budibase.budibase

*Inside `vars/main.yml`*:

    budibase_jwt_secret: d953c4ea298f122721a701551
    budibase_minio_access_key: 6250f5ff106548bf972eba689af50fd4
    budibase_minio_secret_key: e58493ec31da4a6a91f79fa46312daa2
    budibase_redis_password: fcde076a0b5941f592e6b96873b6768a
    budibase_couchdb_user: ec033d50c2a241a5a931c8da16893e1f
    budibase_couchdb_password: 6f46b35d020641b5b529b098e0e94c75
    budibase_internal_api_key: 3ccd101bf6fe49aaa8fd721423885f65

## License

GPLv3

## Author Information

This role was created in 2022 by [Jeff Geerling](https://www.jeffgeerling.com/)
