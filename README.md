# ELK 5.x Vagrant Image

This repo is to make my life with ELK easier. It's been updated to the lastest version of Elastic product, which currently means Elasticsearch 5.0 & Kibana 5.0. Also, just for the testing purposes, it includes an installation of their X-Pack plugin(s).

*The license for X-Pack plugin will expire in one month after this VM has been built.*

## Building the image

```bash
    vagrant up
```

And that's it!

In case you need to check the internals of the installed VM, you can always ssh into the box by:

```bash
    vagrant ssh
```

## Forwarded ports

Port     | Application   | Note                               
---------|---------------|------------------------------------
5601/tcp | Kibana        | Reachable via http://localhost:5601/
9200/tcp | Elasticsearch |
9300/tcp | Elasticsearch Transport|

## Authentication

Because one of plugins installed is a plugin named Shield, providing authentication, you will be required to log on to the Kibana in the VM.

For that reason, here's the default credentials:

 * username: *elastic*
 * password: *changeme*

## Extra Kibana plugins

Apart from X-Pack, there's no extra visualization plugin or application installed. This may change in the future.
