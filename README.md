# 🔑 ftpknocker

ftpknocker is a multi-threaded scanner for finding anonymous FTP servers

[![Code Climate](https://img.shields.io/codeclimate/maintainability/kennell/ftpknocker.svg)]() [![Travis](https://img.shields.io/travis/kennell/ftpknocker.svg)]() [![Codecov](https://img.shields.io/codecov/c/github/kennell/ftpknocker.svg)]() [![PyPI](https://img.shields.io/pypi/v/ftpknocker.svg)]() 

## Donations

Your contribution keeps this project going ❤️ 

* BTC 121QcrzmFsYfxpJYneTS4N6yKDdU8GGfXa
* ETH 0x56Aab3cDA7Ea02953aE394F9ffA3f7b80ed8b6DE
* LTC LerFT8YP7Q9etp2M3EsJxLZJYeFCZLV6wQ

## Install

```
pip install ftpknocker
```

## Usage

```
Usage: ftpknocker [OPTIONS] [TARGETS]...

Options:
  --threads INTEGER         Number of threads to utilize
  --port INTEGER            Port to scan
  --timeout FLOAT           Seconds before timeout
  --shuffle / --no-shuffle  Shuffle target list
  --help                    Show this message and exit.
```

## Usage examples

The syntax for specifying targets is similar to nmap. Here are some examples:

Scan three individual IPs:
```bash
ftpknocker 192.168.1.1 192.168.1.2 192.168.1.3
```

Scan an entire IP-block using [CIDR notation](http://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation). In this example, a total of 256 hosts are scanned:
```bash
ftpknocker 192.168.1.0/24
```

Feed targets from a other program using a pipe (IPs must be sperated by newlines):
```bash
cat mytargets.txt | ftpknocker
```
## Development and testing

1. Clone the repository
2. Install the requirements `pip install -r requirements`
3. Run `pytest`
