# KMITL-Auto-Authen-Mikrotik

A **_Mikrotik script_** that let you automatically authenticate into KMITL network

## Getting started
### Prerequisites
* Mikrotik RouterOS v.6.43 or later
* WinBox

### Installation
1. In WinBox goto System->Scripts in tab Scripts
2. Add *[mikrotik-json-parser](https://github.com/Winand/mikrotik-json-parser)* script to MikroTik
   1. Click plus button to add new script
   2. Use name `JParseFunctions`
   3. Copy source code from [JParseFunctions](https://raw.githubusercontent.com/Winand/mikrotik-json-parser/master/JParseFunctions) and paste into source
   4. Click **OK** to save
3. Add this script to MikroTik
   1. Click plus button to add new script
   2. Use name `Auto-Login-KMITL`
   3. Copy source code from [Auto-Login-KMITL](https://raw.githubusercontent.com/ouoam/KMITL-Auto-Authen-Mikrotik/master/Auto-Login-KMITL) and paste into source
   4. Edit username and password on top of source code
   5. Click **Run Script** and then click **OK** to save

### Usage
When you run this script. Script will create new scheduler to autorun this script on MikroTik startup for auto Auten.
You can view log for more info. Log form this script is start with `Auto-Login`

### Config
You can change config at top of script.
You **can not** change Heartbeat interval, it will use value form authen server.

| Alias | Name | Description |
|:-----:|:----:|-------------|
| `loginUser` | Username | Username to login _(without **@kmitl.ac.th**)_ |
| `loginPass` | Password | Password to login |

## Credit
* **_Member in Network Laboratory_** for [Auto Authen KMITL](https://gitlab.com/networklab-kmitl/auto-authen-kmitl) written in Python language (and some README.md)
* **_[@mayueeeee](https://github.com/mayueeeee)_** for [KMITL-Auto-Authen](https://github.com/mayueeeee/KMITL-Auto-Authen) written in Go language

## Thank
* **_[@Winand](https://github.com/Winand)_** for [mikrotik-json-parser](https://github.com/Winand/mikrotik-json-parser) to parse json in MikroTik
* **_[Burp Suite Community](https://portswigger.net/burp)_** for tool to sniffer communicate with authen server
* **_[FoxyProxy Standard](https://chrome.google.com/webstore/detail/foxyproxy-standard/gcknhkkoolaabfmlnjonogaaifnjlfnp?hl=en)_** for tool to redirect communicate to proxy server
* **_[Postman](https://www.getpostman.com/)_** for tool to simulate communicate with authen server
* **_[NetCat](https://eternallybored.org/misc/netcat/)_** for tool to simulate as authen server
* **_ISAG_** for nice place to stay for write, edit, run and test this script

## Team
* only me

## Disclaimer
This project is only an experiment on KMITL authentication system and it does not provided a bypass for login system
