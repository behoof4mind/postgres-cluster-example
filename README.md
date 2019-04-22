# PostgreSQL cluster example
Test HA cluster, based on Postgres, PgBouncer, Patroni, etcd and VIP-manager.
For test purposes only!

## General description
Some text must be here

## Third-party products list
Some text must be here
### [Vagrant]
Vagrant is a tool for building and managing virtual machine environments in a single workflow. With an easy-to-use workflow and focus on automation, Vagrant lowers development environment setup time, increases production parity, and makes the "works on my machine" excuse a relic of the past.
[More](https://www.vagrantup.com/intro/index.html)
### [PGBouncer]
PgBouncer is a lightweight connection pooler for PostgreSQL.
[More](https://wiki.postgresql.org/wiki/PgBouncer)
### [Patroni]
Patroni is a template for you to create your own customized, high-availability solution using Python and - for maximum accessibility - a distributed configuration store like ZooKeeper, etcd, Consul or Kubernetes. 
[More](https://patroni.readthedocs.io/en/latest/)
### [etcd]
Etcd is a distributed reliable key-value store for the most critical data of a distributed system
[More](https://coreos.com/etcd/docs/latest/)
### [VIP-Manager]
Manages a virtual IP based on state kept in etcd or Consul. Monitors state in etcd
[More](https://github.com/cybertec-postgresql/vip-manager)

## Usage
* install vagrant [vagrantup/installation](https://www.vagrantup.com/docs/installation/)
* install virtual box [virtualbox/installation](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=13&cad=rja&uact=8&ved=2ahUKEwj90-u-0ePhAhXwwcQBHWgmDl8QFjAMegQIBBAB&url=https%3A%2F%2Fwww.virtualbox.org%2Fmanual%2Fch02.html&usg=AOvVaw2MR27hIJR9ea15aOEfQIKg)
* Execute: ```vagrant up --provision```
* Execute: ```vagrant plugin install vagrant-vbguest```
Please notice, that VirtualIP is summarize of last octet if your IP and IPFactor value. [inventory](inventory)
After all you can connect to PGBouncer.

## Troubleshooting
Some text must be here

## Monitoring
Some text must be here

## Additional info
Some text must be here