# HOST DISCOVERY
Used when we conduct internal pentest of entire network of company.
there are many host discovery options in `NMAP` but most effective method was `ICMP echo requests`

```
sudo nmap <target>/24 -Sn -oA tnet | grep for | cut -d" " -f5
```

| Scanning Options | Description                                     |
|------------------|-------------------------------------------------|
| <'target'>/24     | Target network range.                           |
| -sn              | Disables port scanning.                         |
| -oA tnet         | Stores the results in all formats named 'tnet'. |

This scanning method works only if the firewalls of the hosts allow it. Otherwise, we can use other scanning techniques to find out if the hosts are active or not.

# Scan IP List

```
sudo nmap <target> -Sn -oA host
```

```
Offensive404@htb[/htb]$ sudo nmap 10.129.2.18 -sn -oA host 

Starting Nmap 7.80 ( https://nmap.org ) at 2020-06-14 23:59 CEST
Nmap scan report for 10.129.2.18
Host is up (0.087s latency).
MAC Address: DE:AD:00:00:BE:EF
Nmap done: 1 IP address (1 host up) scanned in 0.11 seconds

```
where (-Sn) disable port scanning

If we disable port scan nmap automatically ping with ICMP echo request (-PE) once request sent we except ICMP reply.
the Intersenting part is previous scan did not do that because before nmap could send ICMP echo Request it would send an ARP ping and resulting ARP reply

we can confirm this with `packet-trace` 

```
sudo nmap 10.129.2.18 -sn -oA host --packet-trace

Starting Nmap 7.80 ( https://nmap.org ) at 2025-08-05 00:08 CEST
SENT (0.0074s) ARP who-has 10.129.2.18 tell 10.10.14.2
RCVD (0.0309s) ARP reply 10.129.2.18 is-at DE:AD:00:00:BE:EF
Nmap scan report for 10.129.2.18
Host is up (0.023s latency).
MAC Address: DE:AD:00:00:BE:EF
Nmap done: 1 IP address (1 host up) scanned in 0.05 seconds
```

another technique is `--reason` --- `Displays the reason for specific result.`

for disabling APR request and ARP reply we can use `--disable-arp-ping`
