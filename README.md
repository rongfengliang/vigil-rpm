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

## TroubleShouting

* `not found: "./res/assets/"`

detail info:

```code
vigirl-monitor vigil: right: `true`: assets directory not found: "./res/assets/"', src/main.rs:143:5
Jun 19 15:12:53 vigirl-monitor vigil: note: Run with `RUST_BACKTRACE=1` environment variable to display a backtrace.
Jun 19 15:12:53 vigirl-monitor systemd: vigil.service: main process exited, code=exited, status=101/n/a
Jun 19 15:12:53 vigirl
```

answer:

please provide the  assets path,like below && use absolute path

`/etc/vigil.cfg` file

```code
[assets]

path = "/etc/vigil/res/assets/"
```
