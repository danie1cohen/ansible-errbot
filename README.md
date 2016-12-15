[![Build Status](https://travis-ci.org/danie1cohen/ansible-errbot.svg?branch=master)](https://travis-ci.org/danie1cohen/ansible-errbot)

Errbot
=========

Spin up an errbot installation in a virtual environment.  This has only been
tested with the slack backend.

Requirements
------------

None

Role Variables
--------------

You should define at least these variables to get your configuration up and
running.

    errbot_backend: Slack
    errbot_identity_token: xoxb-11625.....etc
    errbot_bot_admins:
      - "@you"
    errbot_bot_alt_prefixes:
      - "@yourbot"


Errbot defines its configuration in a pure python file: config.py.  That can
make defining variables via ansible a little tricky.  In cases where a string
is always expected, the variable is already surrounded in quotes for you. You
can define your strings in yaml normally.  In some cases, the config variable
is usually a python object, and if you want to pass it a string you must
quote it yourself.

Dependencies
------------

`danie1cohen.virtualenv3`

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
