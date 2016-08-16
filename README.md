synthesize-vars
===============

This role creates facts from two sources: environment variables or ansible variables.

Preference is given to values provided through various environment variables.

Fallback of missing environment variables is through either default values
provided in variables or passed in by playbooks.

These facts are primarily for use in other roles.

It's easy for anyone to modify the role as needed since it's MIT licensed.

Requirements
------------

Tested to run on Linux, FreeBSD, and OS X. Windows is not supported.

Role Variables
--------------

Pass in these values in the playbook:

* default_build_dir
* default_version_type (valid values are "SEMVER" and "YYYY.MM.DD.BUILD")


Dependencies
------------

Role expects to find values for these environment variables:

* BRANCH
* BUILD_NUMBER
* NODE_NAME
* BUILD_USER
* BUILD_URL
* BUILD_NOTES
* VERSION_TYPE

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: coesohq.sib-synthesize-vars,
             default_build_dir: "",
             default_version_type: "YYYY.MM.DD.BUILD" }

License
-------

MIT

Author Information
------------------

Hamza Sheikh
