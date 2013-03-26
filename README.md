vagrant-plugins-env
===================

A simple environment to develop vagrant plugins in. It encapsulates the vagrant environment into an own `.vagrant.d` directory to avoid messing with your day-to-day vagrant config.

This sample uses the [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest) plugin as default.



## Usage

0. `git clone`
  1. edit submodules as needed
  2. edit `Gemfile` as needed
1. `git submodule init`
2. `git submodule update`
3. `bundle install`

To start vagrant use the `bin/vagrant` wrapper!
