# Vagrant CI

**Warning: This box is under heavy development so it's not a complete work yet.**

This is CI box using vagrant and ansible, it could be run as CI server on your local machine. This box contain :

* Ubuntu 14.04
* PHP
* nGinx
* MariaDB
* Mailcathcer
* Ruby
* Apache Ant
* Apache Maven
* NodeJS
* Jenkins

### Sofware

- [Vagrant](http://www.vagrantup.com), tested with v1.7.4
- [VirtualBox](https://www.virtualbox.org), tested with v5.0.0.

### Hardware

- This environment need at least 2GB (2048 KB) RAM for it self, so you need at least 4GB RAM installed at your machine.
- Number of CPUs is 1.
- Video memory is 8MB.
- Storage start from 10 GB (it'll increased by time).

### Preparation

* Make sure you already generate ssh key and add that ssh key to your github account, you can see the tutorial [here](https://help.github.com/articles/generating-ssh-keys/).
* Check your ssh to use agent forwarding, you can see the tutorial [here](https://developer.github.com/guides/using-ssh-agent-forwarding/), and if you already add agent forwarding config but still not working, you can try run `ssh-add -K` at your terminal.

## Installation

1. Clone the repository on your local machine.
2. Go to `/path/of/your/vagrant-ci` with terminal or console.
3. Run `vagrant up` inside that folder and wait until vagrant configuration is completed.
4. Add this to your `/etc/hosts` file :

```
    192.168.56.10  vagrant-ci.dev jenkins.vagrant-ci.dev mail.vagrant-ci.dev
```

## Application

* Jenkins web could be accessed from http://jenkins.vagrant-ci.dev.
* Mailcatcher web could be accessed from http://mail.vagrant-ci.dev.
* MariaDB could be accessed using ssh to vagrant box using `vagrant` as both of username and password, and give `root` for both of username and passwotd to mariadb.

## License

Copyright (c) 2015 rolies106

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

