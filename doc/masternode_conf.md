Masternode config
=======================

Axe Core allows controlling multiple remote masternodes from a single wallet. The wallet needs to have a valid collateral output of 1000 coins for each masternode and uses a configuration file named `masternode.conf` which can be found in the following data directory (depending on your operating system):
 * Windows: %APPDATA%\AxeCore\
 * Mac OS: ~/Library/Application Support/AxeCore/
 * Unix/Linux: ~/.axecore/

`masternode.conf` is a space separated text file. Each line consists of an alias, IP address followed by port, masternode private key, collateral output transaction id and collateral output index.

Example:
```
mn1 127.0.0.2:9937 93HaYBVUCYjEMeeH1Y4sBGLALQZE1Yc1K64xiqgX37tGBDQL8Xg 7603c20a05258c208b58b0a0d77603b9fc93d47cfa403035f87f3ce0af814566 0
mn2 127.0.0.4:9937 92Da1aYg6sbenP6uwskJgEY2XWB5LwJ7bXRqc3UPeShtHWJDjDv 5d898e78244f3206e0105f421cdb071d95d111a51cd88eb5511fc0dbf4bfd95f 1
```

Axe Sentinel is required for proper masternode operation.
Install Sentinel in your data directory following the manual https://github.com/AXErunners/sentinel

_Note: IPs like 127.0.0.* are not allowed actually, we are using them here for explanatory purposes only. Make sure you have real reachable remote IPs in you `masternode.conf`._

The following RPC commands are available (type `help masternode` in Console for more info):
* list-conf
* status
* start-alias \<alias\>
* start-all
* start-missing
* start-disabled
* outputs

Detailed guide https://github.com/AXErunners/axe/wiki/Masternodes
