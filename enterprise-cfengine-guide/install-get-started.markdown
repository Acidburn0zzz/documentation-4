---
layout: default
title: Install and Get Started
published: true
sorting: 10
---

* [Installation][Install and Get Started#Installation]
* [Post-Install Configuration][Install and Get Started#Post-Install Configuration]
	
## Installation ##

### Installing Enterprise Licenses

Before you begin, you should have your license key, unless you only
plan to use the free 25 node license. The installation instructions
will be provided with the key.

### Packages

The CFEngine Enterprise packages are native packages, installed with
your platform's package manager in the usual ways.

## Post-Install Configuration ##

### Change Email Setup After CFEngine Enterprise Installation ###

For Enterprise 3.6.0 local mail relay is used, and it is assumed the server has a proper mail setup.

The default FROM email for all emails sent from the Mission Portal is ```admin@organization.com```. This can be changed on the CFE Server in ```/var/cfengine/httpd/htdocs/application/config/appsettings.php:$config['appemail']```.

### Version your policies

Consider enabling the built-in version control of your policies as
described in
[Version Control and Configuration Policy][Best Practices#Version Control and Configuration Policy]

Whether you do or not, please put your policies in some kind of
backed-up VCS. Losing work because of "fat fingering" `rm` commands is
very, very depressing.

### Review settings

See [The Policy Framework][The Policy Framework] for a full list of all the settings you can configure.
