## Example bird configuration for dn42

* This is the setup I use on my both dn42 routers.
* It is designed to be reused on multiple hosts.
* optimize routes by using bgp community values
* contains example for ibgp/ospf

## Install

On archlinux bird expect the configuration
at /etc/bird.conf and /etc/bird6.conf.
This is NOT the case on debian!

```
$ git clone https://github.com/Mic92/ffhl-bird6.git /etc/bird
$ ln -s /etc/bird/bird.conf /etc/bird.conf
$ ln -s /etc/bird/bird6.conf /etc/bird6.conf
$ export HOST=yourhostname
$ mkdir /etc/bird/peers4-$HOST /etc/bird/peers6-$HOST
$ ln -s /etc/bird/peers4-$HOST /etc/bird/peers4
$ ln -s /etc/bird/peers6-$HOST /etc/bird/peers6
$ cp /etc/bird/local4-template.conf /etc/bird/local4-$HOST.conf
$ cp /etc/bird/local6-template.conf /etc/bird/local6-$HOST.conf
$ ln -s /etc/bird/local4-$HOST.conf /etc/bird/local4.conf
$ ln -s /etc/bird/local6-$HOST.conf /etc/bird/local6.conf
```
