[cmk-apcupsd](http://github.com/aikinaro/cmk-apcupsd) Checkmk package for monitoring UPS managed by apcupsd
=========

Description
---------

This is package for Checkmk which allow to checks status of ups managed by apcupsd demon.
Package contain plugin for checkmk linux agent, templates for pnp4nagios and perfometer plugins.
You can monitor:
* UPS status
* battery charge
* load capacity
* internal temperature
* input, output and battery voltage level
* remaining runtime on battery

Avaliable checks are dependet on which model of ups you have. Package was tested on APC Smart-UPS 2200 RM. 
 

Requirements
---------

1. [Checkmk](https://checkmk.com/download) (tested on 2.0p7 and 2.1)
2. [Apcupsd](http://www.apcupsd.org/)


Installation
-----------

1. Dowload mpk file on host where checkmk is installed and run:
   # Checmk 1.6 and 2.0 syntax
   ```
   mkp install cmk-apcupsd-[VERSION].mpk
   ```

   # old syntax
   ```
   check_mk -P install cmk-apcupsd-[VERSION].mpk
   ```
2. [Optional] adjust voltage values to match local environment
   # FIXME: which file and how?
3. On host which run apcupsd install check_mk_agent, and put agents/plugins/apcupsd from this repo in check_mk_agent plugins directory (/usr/lib/check_mk_agent/plugins/)
4. Rescan services for monitored host


Authors
-------

The current author and maintainer of cmk-apcupsd is Christian Kreidl
(christiankreidl).  In 2021 the project was forked and updated to support
Checkmk 2.0.


The original author of cmk-apcupsd is Michal Skalski (michalskalski).  Between
2018 and 2020, the "repository has been archived by the owner.  It is now
read-only."

 https://github.com/michalskalski/cmk-apcupsd
