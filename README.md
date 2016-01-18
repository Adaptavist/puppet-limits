# Limits module for Puppet
[![Build Status](https://travis-ci.org/Adaptavist/puppet-limits.svg?branch=master)](https://travis-ci.org/Adaptavist/puppet-limits)

## Description
Module for managing pam limits in /etc/security/limits.conf.

## Usage

### limits::fragment - Simple usage

<pre>
  limits::fragment
    "*/soft/nofile":
      value: "1024"
    "*/hard/nofile":
      value: "8192"
  }
</pre>

### Additional parameters: 
- title - should be of the form domain/(hard|soft-)/item if $domain, $type
        and $item are not present
- value - value of limit, use undef to remove the value
- domain - limit domain
- type - limit type (hard|soft|-)
- item - limit item
- limits_file - limits configuration file, default /etc/security/limits.conf

