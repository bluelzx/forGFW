# SpechtLite Config
**Forked and Revised from [HoonHwang/SpechtLiteConf](https://github.com/HoonHwang/SpechtLiteConf)**

This is a template for SpechtLite designed for Chinese users.


- **conf.yaml**: The main configuration file, where all adapters and rules reside. You may want to copy and rename this file if you want to have several different settings to switch between.

- **pollutedip**: The list of DNS polluted IP addresses according to [Wikipedia](https://zh.m.wikipedia.org/zh-cn/域名服务器缓存污染).

- **directlist**: The list of hosts that you want to connect directly, in regular expressions.

- **directiprange**: The list of ip ranges that you want to connect to directly without any proxy.

- **proxylist**: The list of hosts that you want to connect to through proxy, in regular expressions.

- **proxyiprange**: The list of ip ranges that you want to connect to through proxy.

- **rejectlist**: Any hosts you want to block. Currectly it contains a set of ad sites.

- **rejectiprange**: Any IP ranges you want to block. Currectly it contains a set of ad sites.


## Get Up and Running
1. Click **`Open config folder`** and copy all files to that (`.SpechtLite`) folder. 

2. Set up the correct adapter configuration according to your proxy settings. 

3. Click **`Reload config`** to reload your configuration.

4. Start proxy by click the name of the config file in the menu, and check **`Set as system proxy`**. 
> Or you can set it yourself by setting system HTTP/HTTPS proxy to `127.0.0.1:port`, SOCKS5 proxy (this will proxy things such as Mail.app) to `127.0.0.1:port+1` in **System Preferences**.

# WhiteIPList
A PAC(Proxy auto-config) file generator with fetched China IP range, which helps walk around GFW.

* Inspired by https://github.com/fivesheep/chnroutes
* Forked from: https://github.com/Leask/Flora_Pac

## Usage
<pre>
$ git clone https://github.com/everfly/WhiteIPList.git
$ cd WhiteIPList
$ ./whitelist -h
usage: whitelist [-h] [-x [PROXY]] [-p [PORT]]

Generate proxy auto-config rules.

optional arguments:
  -h, --help            show this help message and exit
  -x [PROXY], --proxy [PROXY]
                        Proxy Server, examples:
                            SOCKS5 127.0.0.1:1080;
                            SOCKS 127.0.0.1:1080;
Examples: $ ./whitelist -x 'SOCKS5 127.0.0.1:1080; SOCKS 127.0.0.1:1080 DIRECT'
Default proxy is 'SOCKS5 127.0.0.1:1080; SOCKS 127.0.0.1:1080 DIRECT'
</pre>

## License
The MIT License (MIT)

Copyright (c) 2016
