[cmk-apcupsd](https://github.com/christiankreidl/cmk-apcupsd) Checkmk package for monitoring UPS managed by apcupsd
=========

Description
---------

This is a package for Checkmk which checks status of UPS managed by apcupsd demon.
Package includes a plugin for the checkmk linux agent, templates for pnp4nagios and perfometer plugins.
You can monitor:
* UPS status
* battery charge
* load capacity
* internal temperature
* input, output and battery voltage level
* remaining runtime on battery

Available checks are dependent on which model UPS you have. Package was tested on APC Smart-UPS 2200 RM and Smart-UPS 1500.
 

Requirements
---------

1. [Checkmk](https://checkmk.com/download) (tested on 2.0p7, 2.0p27, 2.1p2, and 2.1p10)
2. [Apcupsd](http://www.apcupsd.org/)


Installation
-----------

1. Download MKP file on host where checkmk is installed and run:
   #### Checkmk 1.6 and 2.0 syntax
   ```
   mkp install cmk-apcupsd-[VERSION].mpk
   ```

   #### Older syntax
   ```
   check_mk -P install cmk-apcupsd-[VERSION].mpk
   ```
2. [Optional] adjust voltage values to match local environment <br/>
   **FIXME: add more details**
3. On host which run apcupsd install check_mk_agent, and put agents/plugins/apcupsd from this repo in check_mk_agent plugins directory (/usr/lib/check_mk_agent/plugins/)
4. Rescan services for monitored host


Authors
-------

The current author and maintainer of *cmk-apcupsd* is Christian Kreidl
(christiankreidl).  In 2021 the project was forked and updated to support
Checkmk 2.0.


The original author of *cmk-apcupsd* is Michal Skalski (michalskalski).  Between
2018 and 2020, the "repository has been archived by the owner.  It is now
read-only."

 https://github.com/michalskalski/cmk-apcupsd
