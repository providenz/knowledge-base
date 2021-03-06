
# CFEngine 3 #

_CFEngine is an IT infrastructure automation framework that helps engineers, system administrators and other stakeholders in an IT system to manage and understand IT infrastructure throughout its lifecycle. CFEngine takes systems from Build to Deploy, Manage and Audit. [<http://cfengine.com/what-is-cfengine>]_

## URL ##

[CFEngine Downloads](http://cfengine.com/downloads)

[Latest Debian Packages](http://cfengine.com/pub/apt/pool/main/c/cfengine-community/)

[CFEngine reference manual](http://cfengine.com/manuals/cf3-reference)

## cf-sketch ##

[Installing cf-sketch](https://github.com/cfengine/design-center/wiki/Installing-cfsketch)

cf-sketch is written in Perl.

Currently there is no Debian packages available.

### Manual installation ###

Install some dependencies :

```
aptitude install libcrypt-ssleay-perl libterm-readline-gnu-perl
```

Get last version from GitHub :

```
wget --no-check-certificate https://github.com/downloads/cfengine/design-center/cf-sketch-latest.tar.gz
tar xf cf-sketch-latest.tar.gz
```

Use make to install in `/usr/local/bin` by default :

```
cd cf-sketch
make install
```

## Logging ##

See <http://cfengine.com/manuals/cf3-Reference#Text-logs>.

`cf-serverd` logs incoming requests using **syslog**.

`/var/cfengine/cf3.HOSTNAME.runlog` is the main logfile for looking at CFEngine activity.

`/var/cfengine/cfagent.HOSTNAME.log` could be deleted (obsolete).

`/var/cfengine/promise_summary.log` is useful to check that all promises are kept.
It could be monitored by a Nagios plugin.

