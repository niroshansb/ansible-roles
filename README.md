# ansible-roles
MapMint installer

Use [ansible](http://www.ansible.com/) to deploy a MapMint instance on
[Debian Jessie 8.2](https://www.debian.org/releases/stable/)  and
[Ubuntu 14.04.3 LTS](http://www.ubuntu.com/download/server).

Edit the ```debian/dependencies/vars/main.yml``` and set the ```serverid```
variable to ```<HOST>:<PORT>``` where ```<HOST>``` and ```<PORT>```are
respectiveley the hostname (or ip address) and the port of the web server to reach
the instance. The ```<PORT>```is optional, for a local setup, you can
simply set the value to ```localhost```.

Run the following commands from any host allowed to access, as root
through ssh, the host where to deploy the MapMint instance.

```
cd debian
ansible-playbook -s server.yml -u root
```
