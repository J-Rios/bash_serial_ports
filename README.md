# bash_serial_ports

Bash scripts to ease manage, check, open, close, write, read and log from Serial ports.

It allows to open a Serial port and log it with a timestamp to a file at same time.

The scripts create an upper layer that call and use [grabserial](https://github.com/tbird20d/grabserial).

## Installation

1. Get and install grabserial:

```bash
git clone https://github.com/tbird20d/grabserial
cd grabserial
git checkout v2.1.0
sudo cp -a grabserial /usr/local/sbin/
sudo chmod +x /usr/local/sbin/grabserial
cd ..
rm -rf ./grabserial
```

2. Get current repository and install the scripts:

```bash
https://github.com/J-Rios/bash_serial_ports
cd bash_serial_ports
sudo cp -a ./serial_* /usr/local/sbin/
sudo chmod +x /usr/local/sbin/serial_*
cd ..
rm -rf ./bash_serial_ports
```

## Usage

- List detected Serial ports on the system:

```bash
serial_list
```

- Check if port /dev/ttyUSB0 is open:

```bash
serial_check ttyUSB0
```

- Open a serial port:

```bash
serial_open 19200 ttyUSB0
```

- Close a Serial port:

```bash
serial_close ttyUSB0
```
