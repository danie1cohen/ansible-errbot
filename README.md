Errbot
=========

Spin up an errbot installation in a virtual environment.  This has only been
tested with the slack backend.

Requirements
------------

None

Role Variables
--------------

You should define at least these variables, to get your configuration up and
running.

project: errbot
errbot_root: /opt/errbot
errbot_backend: Slack
errbot_identity_token: xoxb-11625.....etc
errbot_bot_admins: ('@you',)
errbot_bot_alt_prefixes: ('@yourbot',)

Dependencies
------------

danie1cohen.virtualenv3

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - danie1cohen.errbot

License
-------

BSD

Author Information
------------------

[Dan Cohen](www.dancohen.io)
