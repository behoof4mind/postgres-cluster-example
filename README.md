# PostgreSQL cluster example
Some text must be here

## General description
Some text must be here
## Third-party products list
Some text must be here
### [Vagrant]
Some text must be here
### [PGBouncer]
Some text must be here
### [Patroni]
Some text must be here
### [etcd]
Some text must be here
### [confd]
Some text must be here
### [HAProxy]
Some text must be here
### [Keepalived]
Some text must be here

## Usage
* install vagrant
* install virtual box
* Vagrantfile:

```yaml
Vagrant.configure("2") do |config|
  config.vm.box = "generic/alpine39"
end
```
* vagrant plugin install vagrant-vbguest
* vagrant up
* vagrant provision

## Troubleshooting
Some text must be here

## Monitoring
Some text must be here

## Additional info
Some text must be here