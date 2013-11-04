wlux_env
========

Vagrantfile and associated Chef cookbooks for WebLabUX Development

# Requirements

* Local Ruby Environment with Bundler (Ruby 2.0.x preferred; 1.9+ should work)
* VirtualBox Installed
* [Vagrant](http://www.vagrantup.com/) Configured

## Prior to First Run

** IMPORTANT **

Clone or symlink your copies of the `wlux_test_server` and `wlux_test_site` into
the `weblabux/` in this repository. These files will be mounted by the virtual
machine, and changes synced back-and-forth between the two. 

## Setup

0. `bundle install`
1. `vagrant plugin install vagrant-berkshelf`
2. `vagrant box add http://files.vagrantup.com/precise64.box`
3. `vagrant up`
4. Pray.

