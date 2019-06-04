Role Name
=========

Install and configure an [Ethercalc](https://ethercalc.net/) service.

The role will setup an Ethercalc server running locally on 0.0.0.0:8000

We recommend using a Redis server to save the data

A webserver will need to be configure to point to your Ethercalc instance

Role Variables
--------------

* `ethercalc_required_packages: ['git','nodejs','gcc-c++' ]`
* `ethercalc_repository: "https://github.com/audreyt/ethercalc.git"`
* `ethercalc_repository_key_file: ""`
* `ethercalc_repository_version: "master"`
* `ethercalc_user: "ethercalc"`
* `ethercalc_group: "{{ ethercalc_user }}"`
* `ethercalc_home: "/home/ethercalc"`
* `ethercalc_path: "{{ ethercalc_home }}/ethercalc"`
* `ethercalc_use_redis: true`
* `ethercalc_spreadsheets_seconds_to_expire: 2592000`

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: broferek.ethercalc

License
-------

GPLv3
