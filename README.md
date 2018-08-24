# vagrant-aws
This repo is a collection of Vagrantfile's to work with AWS instances
*I've only worked from a Windows 10 machine, the Vagrantfile's should work elsewhere, but I have not tried them put.*

**There are different Vagrantfile's for each scenario:**

- `Vagrantfile` - spinning up a basic t2.micro AMI (Amazon Machine Image) in AWS
- [`docker-compose/Vagrantfile`](docker-compose/README.md) - includes provisioning t2.micro AMI with docker, docker-compose and running docker-compose.yml

**Relater blog posts for the above Vagrant files are at:**

- https://melissapalmer.github.io/devops/2018/08/03/docker-4-unix-on-windows.html 