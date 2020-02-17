# Description

A very fast and smart web-dir/file enumeration tool written in C for the lulz.

# Usage

```
$ lulzbuster -H
    __      __      __               __
   / /_  __/ /___  / /_  __  _______/ /____  _____
  / / / / / /_  / / __ \/ / / / ___/ __/ _ \/ ___/
 / / /_/ / / / /_/ /_/ / /_/ (__  ) /_/  __/ /
/_/\__,_/_/ /___/_.___/\__,_/____/\__/\___/_/

        --==[ by nullsecurity.net ] ==--

usage

  lulzbuster -s <arg> [opts] | <misc>

target options

  -s <url>       - start url to begin scan with

http options

  -h <type>      - http request type (default: GET) - ? to list types
  -x <code>      - exclude http status codes (default: 404,503 - multi
                   codes separated by ',')
  -f             - follow http redirects. hint: better try appending a '/'
                   with '-A' option first instead of using '-f'
  -F <num>       - num level to follow http redirects (default: 0)
  -u <str>       - user-agent string (default: built-in windows firefox)
  -U             - use random built-in user-agents
  -c <str>       - pass custom header(s) (e.g. 'Cookie: foo=bar; lol=lulz')
  -a <creds>     - http auth credentials (format: <user>:<pass>)
  -r             - turn on auto update referrer
  -j <num>       - define http version (default: curl's default) - ? to list

timeout options

  -D <num>       - num seconds for delay between requests (default: 0)
  -C <num>       - num seconds for connect timeout (default: 10)
  -R <num>       - num seconds for request timeout (default: 30)
  -T <num>       - num seconds to give up and exit lulzbuster completely
                   (default: none)

tuning options

  -t <num>       - num threads for concurrent scanning (default: 30)
  -g <num>       - num connection cache size for curl (default: 30)
                   note: this value should always equal to -t's value

other options

  -w <file>      - wordlist file
                   (default: /usr/local/share/lulzbuster/lists/medium.txt)
  -A <str>       - append any words separated by comma (e.g. '/,.php,~bak)
  -p <addr>      - proxy address (format: <scheme>://<host>:<port>) - ? to
                   list supported schemes
  -P <creds>     - proxy auth credentials (format: <user>:<pass>)
  -i             - insecure mode (skips ssl/tls cert verification)
  -S             - smart mode aka compare response sizes when wildcard was
                   detected, etc. (use this if speed is not 1st priority!)
  -n <str>       - nameservers (default: '1.1.1.1,8.8.8.8,208.67.222.222'
                   multi separated by '.')
  -l <file>      - logfile for found valid urls (default: stdout)

misc

  -X             - print built-in user-agents
  -V             - print version of lulzbuster and exit
  -H             - print this help and exit
```

# Author

noptrix

# Distros

[![Packaging status](https://repology.org/badge/vertical-allrepos/lulzbuster.svg)](https://repology.org/project/lulzbuster/versions)

# Disclaimer

We hereby emphasize, that the hacking related stuff on
[nullsecurity.net](http://nullsecurity.net) is only for education purposes.
We are not responsible for any damages. You are responsible for your own
actions.