# LEXDEE

## Installing LXD from packages
Add the current user to sudo if not already, to avoid prefix'g sudo for every lxc command
> usermod -aG sudo mintman



Lxd is by defaut available on new versions of releases.
`lxd --version`

We can choose a desired version & easy to manage by using snap pkg.

`snap install lxd`

```
Alternatively, pass parameters:
--channel=4.0/stable for the LXD 4.0 LTS release,
--channel=3.0/stable for the LXD 3.0 LTS release or
--channel=2.0/stable for the LXD 2.0 LTS release.
```

Cross check snap pkg is install - 
`snap list`
View snap info
`snap info lxd`


Now check the lxd & lxc version
```
lxd --version
lxc --version
```

And their locations
```
which lxd
which lxc
```

Migrate existing lxd data over (if already present)
`snap lxd.migrate`

Initialize lxd with storage, network & other configurations.
`lxd init'

Lets first check the cloud-images.
`lxc remote list`

To download a specific image, launch by passing the name
`lxc launch ubuntu:18.04` creates a random name for container
`lxc launch ubuntu:18.04 myubuntu1` creates with a name 'myubuntu1'
`lxc launch images:centos/7 mycentos1` format for other than ubuntu

Check list of image slocally available
```
lxc image list
lxc image list ubuntu:
lxc image list images:cent
```


