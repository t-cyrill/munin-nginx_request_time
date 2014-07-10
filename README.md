munin-nginx_request_time
========================

Munin plugin for nginx request time

Modes
----------------

* Default

min, median, 90th percentile, 95th percentile

* max

max

Usage
----------------

munin-nginx_request_time plugin needs Statistics modules.

```
sudo cpanm install Statistics::Lite
sudo cpanm install Statistics::Descriptive
```

And then,

```
ln -s nginx_request_time /etc/munin/plugins/nginx_request_time
ln -s nginx_request_time /etc/munin/plugins/nginx_request_time_max
```

Configration
----------------

* logfile

ie. /var/log/nginx/access.log

* loglimit

ie. 1000

### Example

```
[nginx_request_time]
    env.logfile /var/log/nginx/access.log
    env.loglimit 1000
```
