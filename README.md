Chef-mode is an Emacs minor mode to make editing
[Opscode Chef](http://www.opscode.com/chef/)
[repositories](http://wiki.opscode.com/display/chef/Chef+Repository)
easier.

It defines a minor mode, chef-mode, and a corresponding
global-chef-mode, with two keybindings:

* C-c C-c (M-x chef-knife-dwim) - when editing part of chef repository
(cookbook, data bag item, node/role/environment definition), uploads
that part to the Chef Server by calling appropriate knife command
* C-c C-k (M-x knife) - runs a user-specified knife command

The library detects bundler and, if Gemfile is present on top-level of
the Chef repository, runs 'bundle exec knife' instead of plain
'knife'.

If `chef-use-rvm` is non-nil, it talks with
[rvm.el](https://github.com/senny/rvm.el) to use proper Ruby and
gemset.
