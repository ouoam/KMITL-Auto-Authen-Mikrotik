# KMITL-Auto-Authen-Mikrotik

A **_Mikrotik script_** that let you automatically authenticate into KMITL network

## Getting started
### Prerequisites
* Mikrotik RouterOS v.6.43 or later

### Installation & Upgrade
1. Login into Mikrotik and open new terminal
2. Copy and Pase this script (If use terminal in winbox **Don't use Ctrl-V**, use right click and pase)
```
/tool fetch url=https://raw.githubusercontent.com/ouoam/KMITL-Auto-Authen-Mikrotik/master/Auto-Login-KMITL;
/import file-name=Auto-Login-KMITL;
```
3. If first time install, this script will ask for username and password in terminal.

### Usage
When you run this script. This script will create new scheduler for auto Auten.
You can view log for more info. Log from this script is start with `Auto-Login`

### Config
You can change config at System->Scripts and select scripts name AutoLogin-Config.
You **can not** change Heartbeat interval, it will use value form authen server.

| Name | Description |
|:----:|-------------|
| `username` | Username to login _(without **@kmitl.ac.th**)_ |
| `password` | Password to login |

## Credit
* **_Member in Network Laboratory_** for [Auto Authen KMITL](https://gitlab.com/networklab-kmitl/auto-authen-kmitl) written in Python language (and some README.md)
* **_[@mayueeeee](https://github.com/mayueeeee)_** for [KMITL-Auto-Authen](https://github.com/mayueeeee/KMITL-Auto-Authen) written in Go language

## Thank
* **_[Postman](https://www.getpostman.com/)_** for tool to simulate communicate with authen server
* **_[NetCat](https://eternallybored.org/misc/netcat/)_** for tool to simulate as authen server

## Team
* only me

## Disclaimer
This project is only an experiment on KMITL authentication system and it does not provided a bypass for login system
