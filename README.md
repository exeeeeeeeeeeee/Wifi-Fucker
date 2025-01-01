# Wifi-Fucker
Jamming wifi devices using ARP spoofing.
## Installation

 1. Clone this repository
 ``
 git clone https://github.com/exeeeeeeeeeeee/Wifi-Fucker.git
 ``
 
 2. Just follow the instructions for use.
 ## Usage
 ```
wifi-fucker.py [-h] [-i INTERFACE] [--attackermac MAC] [--gatemac MAC]
               [--targetmac MAC] [--gateip IP] [--interval TIME] [-d]
               TARGET_IP

Execute ARP Cache Poisoning attacks (a.k.a "ARP Spoofing") on local networks.

positional arguments:
  TARGET_IP                    IP address currently assigned to the target.

optional arguments:
  -h, --help            show this help message and exit
  -i INTERFACE, --interface INTERFACE
                        Interface on the attacker machine to send packets
                        from.
  --attackermac MAC     MAC address of the NIC from which the attacker machine
                        will send the spoofed ARP packets.
  --gatemac MAC         MAC address of the NIC associated to the gateway.
  --targetmac MAC       MAC address of the NIC associated to the target.
  --gateip IP           IP address currently assigned to the gateway.
  --interval TIME       Time in between each transmission of spoofed ARP
                        packets (defaults to 0.5 seconds).
  --disassociate        Execute a disassociation attack in which a randomized
                        MAC address is set for the attacker machine,
                        effectively making the target host send packets to a
                        non-existent gateway.
```
## Example
```
~$ sudo python3 arpspoof.py {target ip}

[>>>] ARP Spoofing configuration:
    [+] Interface       .....................eth0
    [+] Attacker MAC    ........08:92:27:dc:3a:71
    [+] Gateway IP      .................10.0.1.1
    [+] Gateway MAC     ........52:93:d0:92:c5:06
    [+] Target IP       .................10.0.1.6
    [+] Target MAC      ........91:8b:28:93:af:07

[!] ARP packets ready. Execute the attack with these settings? (Y/N) y

[+] ARP Spoofing attack initiated. Press Ctrl-C to abort.
```
## License
This project is licensed under the terms of the GNU Affero General Public License (AGPL) version 3 or later. See the [LICENSE](./LICENSE) file for details.
## Copyright
This project is based on the original work by [EONRaider](https://github.com/EONRaider) 
Modified by [exeeeeeeeeeeee](https://github.com/exeeeeeeeeeeee).
