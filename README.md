munin-nginx_request_time
========================

Munin plugin for nginx request time

![munin-nginx_request_time example](https://raw.githubusercontent.com/t-cyrill/munin-nginx_request_time/master/images/example.png "munin-nginx_request_time example")


Modes
----------------

### Default

 * min, median, 90th percentile, 95th percentile

### max

 * max

Usage
----------------

munin-nginx_request_time plugin needs Statistics modules.

```
sudo cpanm File::ReadBackwards
sudo cpanm Statistics::Lite
sudo cpanm Statistics::Descriptive
```

And then,

```
ln -s nginx_request_time /etc/munin/plugins/nginx_request_time
ln -s nginx_request_time /etc/munin/plugins/nginx_request_time_max
```

Configration
----------------

### logfile

* ie. /var/log/nginx/access.log

### loglimit

* ie. 1000

### Example

```
[nginx_request_time]
    env.logfile /var/log/nginx/access.log
    env.loglimit 1000
```
