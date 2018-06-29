# MMDVM_Bridge-Dashboard
Dashboard for MMDVM_Bridge
==================================

About
=====
MMDVM_Bridge-Dashboard is a web-dashboard for visualization of different data like
system temperature, cpu-load ... and it shows a last-heard-list.

It relies on MMDVM_Bridge 


This is a fork ot the MMDVMHost-Dashboard that has been modified to work with MMDVM_Bridge.
This is a work in progress and we modify the screen for better MMDVM_Bridge visibility.
Thanks to Kim DG9VH for a great dashboard!

Based on G4KLX code, mod by EA4GKQ

Required are
============
* Webserver like lighttpd or similar
* php5
* if using sqlite3-database name resolving sqlite3 and php5-sqlite also needed

Installation
============
* Please ensure to not put loglevels at 0 in MMDVM_Bridge.ini.
* Copy all files into your webroot and enjoy working with it.
* Create a config/config.php by calling setup.php and giving suitable values
* If Dashboard is working, remove setup.php from your webroot

For detailled installation see `linux-step-by-step.md` within this repository.

Usage
=====
To use the dashboard simply call the corresponding address in a webbrowser. The webbrowser has to be javascript-enabled because of the usage of DataTables, that would only be functional with Javascript enabled for this site!

Features
========
At the moment there are several information-sections shown:
* System Info: 
  Here you'll find live info about the host-system itself like CPU-freq, temperature, system-load, cpu-usage, uptime and cpu-idle-time.
* Repeater Info:
  Here are some basic repeater info and link-states
* Enabled Modes
  This is a list of enabled modes. If green, it's enabled, if grey, it's disabled. If it is red, there is an error-state with MMDVM_Bridge or ircddbgateway.
* Last Heard List of today's x callsigns:
  This is a list of the last x callsigns heard in general in the system over all modes and directions. X is to be configured in /config/config.php
* Today's last 10 local transmissions:
  For better debugging/calibrating etc. the last 10 local transmissions (RF-side of the repeater) are listed.

New features by EA4GKQ
======================
* Buttons toolbar, security-hint: to make this function secure, please enable htpasswd-function for folder "scripts"!
* LastHeard table are sorted 
* Some mods to improve mobile experience

