[![Build Status](https://travis-ci.org/lasdolphin/infra-db.svg?branch=master)]
(https://travis-ci.org/lasdolphin/infra-db)


infa-db

=========

db role for infra rep
(https://travis-ci.org/lasdolphin/infra)
homework for otus.ru devops course

Requirements
------------

no req


Role Variables
--------------

mongo_bid_ip

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---
- name: Configure db host
  hosts: tag_reddit-db-{{ env }}
  # hosts: tag_reddit-db-stage
  gather_facts: false
  become: true
  pre_tasks:
    - name: Install python for Ansible
      raw: test -e /usr/bin/python || (apt -y update && apt install -y python-minimal)
      changed_when: false
  roles:
    - db


License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
