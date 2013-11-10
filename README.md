wlux_env
========

Vagrant for WebLabUX Development

# Requirements

* Local Ruby Environment with Bundler (Ruby 2.0.x preferred; 1.9+ should work)
    1. Those on Windows can use [RubyInstaller](http://rubyinstaller.org/),
       \*nix platforms should use your distribution's package manager or default
       Ruby installation.
    2. Once Ruby is installed, run `gem install bundler` to install Bundler
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads) (~> 4.3.x) Installed
* [Vagrant](http://www.vagrantup.com/) (~> 1.3.2) Installed
    - If you'd like to learn more about Vagrant, there is [comprehensive
      documentation](http://docs.vagrantup.com/v2/) and a fantastic explanation of
      [Why Vagrant Rocks](http://docs.vagrantup.com/v2/why-vagrant/index.html)
      for both developers and designers.

## Prior to First Run

** IMPORTANT **

Clone or symlink your copies of the `wlux_test_server` and `wlux_test_site` into
the `weblabux/` in this folder. This path will be mounted by the virtual
machine inside the LAMPP `htdocs` path. All changes on your local filesystem
will be reflected on the VM, and vise-versa.

## Setup

0. `bundle install`
1. `vagrant plugin install vagrant-berkshelf`
2. `vagrant box add http://files.vagrantup.com/precise64.box`
3. `vagrant up`
4. Pray.

