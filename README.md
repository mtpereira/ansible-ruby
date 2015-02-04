Ruby [![Build Status](https://travis-ci.org/mtpereira/ansible-ruby.svg)](https://travis-ci.org/mtpereira/ansible-ruby)
=========

Installs Ruby from a custom repository. Default values install Ruby 1.9.3 from [Brightbox repository](https://www.brightbox.com/docs/ruby/ubuntu/).

Requirements
------------

None.

Role Variables
--------------

* `ruby_package_name`: Package name that provides Ruby. Defaults to `ruby1.9.3`.
* `ruby_dev_package_name`: Package name that provides Ruby development libs. Defaults to `ruby1.9.1-dev`.
* `ruby_repo_url`: Repository URL for package installation. Defaults to `http://ppa.launchpad.net/brightbox/ruby-ng/ubuntu/`.
* `ruby_repo_key_url`: GPG key URL for repository validation. Defaults to `http://keyserver.ubuntu.com:11371/pks/lookup?op=get&search=0xF5DA5F09C3173AA6`.
* `ruby_repo_key_server`: GPG key server URL for repository validation. Used in conjunction with `ruby_repo_key_id`. If these two variables are defined, do not define `ruby_repo_key_url`.
* `ruby_repo_key_id`: GPG key ID for repository validation. Used in conjunction with `ruby_repo_key_server`. If these two variables are defined, do not define `ruby_repo_key_url`.
* `ruby_alternatives_ruby_path`: Ruby's binary path for Debian's Alternatives System. Used for setting the installed Ruby as the system's default.
* `ruby_alternatives_gem_path`: Gem's binary path for Debian's Alternatives System. Used for setting the installed Gem as the system's default.


Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: mtpereira.ruby, ruby_package_name: "ruby2.2", ruby_dev_package_name: "ruby2.2-dev" }

License
-------

BSD

Author Information
------------------

Thanks to [Brightbox](https://www.brightbox.com/) for the Ruby packages repository.

[GitHub project page](https://github.com/mtpereira/ansible-ruby)

[Manuel Tiago Pereira](http://mtpereira.github.io)
