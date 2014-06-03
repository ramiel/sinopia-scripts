SINOPIA SERVICE
===============

Script for running [sinopia](https://github.com/rlidwka/sinopia/) server as demon

User
----

This script run sinopia under `sinopia` user, you should create it

```bash
adduser --no-create-home --disabled-login sinopia
```

Copy service to init.d

```bash
sudo cp service/sinopia /etc/init.d/sinopia
```

We need also some directories to store configuration and packages

```bash
sudo mkdir /etc/sinopia
sudo mkdir /etc/sinopia/storage
sudo mv config.yaml /etc/sinopia/
sudo chown root:sinopia /etc/sinopia/ -R
sudo chmod g+w /etc/sinopia/storage
```

You should modify `/etc/sinopia/config.yaml` for your needs

Start it!

```bash
sudo /etc/init.d/sinopia start
```

Author
-----

[Fabrizio "ramiel" Ruggeri](http://www.ramielcreations.com)
