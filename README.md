# Known Vagrant 

This is a Known vagrant virtual machine install, taken from the original files in Known as part of a cleanup.

## Usage

* Download and install [Virtualbox](https://www.virtualbox.org)
* Download and install [vagrant](https://www.vagrantup.com/downloads.html), and the guest extensions.
  * You may find you need to forcibly install the guest extensions:
  
```
vagrant plugin install vagrant-vbguest
vagrant vbguest
```
* Download and install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) (instructions say install via pip, however I used ```brew install ansible```)
* Clone known into ```Known```
* Edit your ```/etc/hosts``` and add the line

```
192.168.33.33	withknown
```

* Run ```vagrant up```
* Connect to your site on "http://withknown"
