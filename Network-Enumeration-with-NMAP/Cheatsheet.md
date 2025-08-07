## Target and Scan Type

| Nmap Option              | Description                                                             |
|--------------------------|-------------------------------------------------------------------------|
| 10.10.10.0/24            | Target network range.                                                   |
| -sn                      | Disables port scanning.                                                 |
| -Pn                      | Disables ICMP Echo Requests.                                            |
| -n                       | Disables DNS Resolution.                                                |
| -PE                      | Performs the ping scan using ICMP Echo Requests.                        |
| --packet-trace           | Shows all packets sent and received.                                    |
| --reason                 | Displays the reason for a specific result.                              |
| --disable-arp-ping       | Disables ARP Ping Requests.                                             |
| --top-ports=<num>        | Scans the specified top ports defined as most frequent.                 |
| -p-                      | Scan all ports.                                                         |
| -p22-110                 | Scan all ports between 22 and 110.                                      |
| -p22,25                  | Scans only the specified ports 22 and 25.                               |
| -F                       | Scans top 100 ports.                                                    |
| -sS                      | Performs a TCP SYN scan.                                                |
| -sA                      | Performs a TCP ACK scan.                                                |
| -sU                      | Performs a UDP scan.                                                    |
| -sV                      | Scans discovered services for their versions.                           |
| -sC                      | Performs a script scan using default scripts.                           |
| --script <script>        | Performs a script scan using specified scripts.                         |
| -O                       | Performs OS detection to determine target OS.                           |
| -A                       | Performs OS detection, service detection, and traceroute scans.         |
| -D RND:5                 | Uses 5 random decoys during scan.                                       |
| -e                       | Specifies the network interface used for the scan.                      |
| -S 10.10.10.200          | Specifies the source IP address for the scan.                           |
| -g                       | Specifies the source port for the scan.                                 |
| --dns-server <ns>        | Uses the specified DNS server for resolution.                           |


## Output Options

| Nmap Option                     | Description                                                    |
|----------------------------------|----------------------------------------------------------------|
| --max-retries <num>             | Sets the number of retries for specific port scans.            |
| --stats-every=5s                | Displays scan status every 5 seconds.                          |
| -v / -vv                        | Displays verbose output.                                       |
| --initial-rtt-timeout 50ms      | Sets initial RTT timeout.                                      |
| --max-rtt-timeout 100ms         | Sets maximum RTT timeout.                                      |
| --min-rate 300                  | Sends at least 300 packets per second.                         |
| -T <0-5>                        | Sets the timing template (0: slowest, 5: fastest/aggressive).  |


## Performance Options

| Nmap Option                     | Description                                                    |
|----------------------------------|----------------------------------------------------------------|
| --max-retries <num>             | Sets the number of retries for specific port scans.            |
| --stats-every=5s                | Displays scan status every 5 seconds.                          |
| -v / -vv                        | Displays verbose output.                                       |
| --initial-rtt-timeout 50ms      | Sets initial RTT timeout.                                      |
| --max-rtt-timeout 100ms         | Sets maximum RTT timeout.                                      |
| --min-rate 300                  | Sends at least 300 packets per second.                         |
| -T <0-5>                        | Sets the timing template (0: slowest, 5: fastest/aggressive).  |
