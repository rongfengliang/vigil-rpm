# vigil-rpm

> rpm for vigil

## Usage

* install package

```code
wget https://github.com/rongfengliang/vigil-rpm/releases/download/v1.4/vigil-v1.4-1.x86_64.rpm

yum install -y vigil-v1.4-1.x86_64.rpm
```

* vigil config file

config file for vigil in  `/etc/vigil.cfg` for more conf you can see `https://github.com/valeriansaliou/vigil`


* service start

```code
systemctl start vigil
```

* config ui template

vigil template && resource  in `/etc/vigil/res`

* auto start when reboot

```code
systemctl  enable vigil
```

## some notes

this version support multi email send config

```code
[notify.email]
from = "status@crisp.chat"
to = "status@crisp.chat,status2@crisp.chat,status@crisp.chat"
```