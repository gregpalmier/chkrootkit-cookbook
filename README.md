chkrootkit Cookbook
===================

[![Build Status](https://secure.travis-ci.org/gregpalmier/chkrootkit-cookbook.png)](http://travis-ci.org/gregpalmier/chkrootkit-cookbook)

Chef cookbook for the chkrootkit scanner

Requirements
------------
Only tested with Ubuntu 12 vagrant box so far

https://opscode-vm.s3.amazonaws.com/vagrant/opscode-ubuntu-12.04-chef11

Attributes
----------

e.g.
#### chkrootkit::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['chkrootkit']['run_daily']</tt></td>
    <td>Boolean</td>
    <td>whether to run daily or not</td>
    <td><tt>default</tt></td>
  </tr>
  <tr>
    <td><tt>['chkrootkit']['run_daily_opts']</tt></td>
    <td>string</td>
    <td>whether to run quietly</td>
    <td><tt>-q</tt></td>
  </tr>
  <tr>
    <td><tt>['chkrootkit']['diff_mode']</tt></td>
    <td>Boolean</td>
    <td>mode.  Not much here yet.</td>
    <td><tt>false</tt></td>
  </tr>
</table>

Usage
-----

Just include `chkrootkit` in your node's `run_list` OR break it out into a role of it's own:

```json
name "chkrootkit"
description "chkrootkit config"
run_list(
    "recipe[chkrootkit]",
)

default_attributes(
    :chkrootkit => { :run_daily => "true" }
)
```

Contributing
------------
TODO: (optional) If this is a public cookbook, detail the process for contributing. If this is a private cookbook, remove this section.

e.g.
1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
License: Nothing here.  Take it and do what you wish.
Authors: Greg Palmier

