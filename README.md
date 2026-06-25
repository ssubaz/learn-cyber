# Cybersecurity Training Notes – June 2026

## Rooms to Be Completed
* [x] [Ohsint](https://tryhackme.com/room/ohsint/)
* [x] [Sakura](https://tryhackme.com/room/sakura/)
* [x] [SearchLight](https://tryhackme.com/room/searchlightosint/)
* [ ] [Kenobi](https://tryhackme.com/room/kenobi/)
* [ ] [Vulnversity](https://tryhackme.com/room/vulnversity/)
* [x] [Blue](https://tryhackme.com/room/blue/)
* [ ] [Ice](https://tryhackme.com/room/ice/)
* [x] [PickleRick](https://tryhackme.com/room/picklerick/)
* [ ] [Wgel CTF](https://tryhackme.com/room/wgelctf/)
* [x] [Crack The Hash](https://tryhackme.com/room/crackthehash/)
* [x] [c4ptur3-th3-fl4g](https://tryhackme.com/room/c4ptur3th3fl4g/)
* [ ] [Bolt](https://tryhackme.com/room/bolt/)
* [x] [Cicada-3301 Vol:1](https://tryhackme.com/room/cicada3301vol1/)
* [ ] [Basic Pentesting](https://tryhackme.com/room/basicpentestingjt/)
* [x] [Lian Yu](https://tryhackme.com/room/lianyu/)

---

## Nmap Commands

1. `nmap -p 500-1000 target machine’s ip`
2. `nmap -sn ip address` (for host discovery)
3. `nmap -iL targets.txt`
4. `nmap -PS -sn target ip` (can mention port number after 22 to send the packets. If not mentioned, it sends to port number 80) – (`-PU` and `-PA` is used for UDP protocols)
5. `nmap -sT target_ip_address`
6. `nmap -sU TARGET` (send packets to all udp ports)
7. `nmap -sL TARGET` (scans for hosts which are about to be scanned by nmap without scanning them)
8. `nmap -sn target` (for scans only live targets without port scanning)
9. `nmap -sN target` (sends null packets to the target)
10. `nmap -sA` (acknowledgement packet)
11. `nmap -sF target` (finish packet) (port is open if we don’t get any response)
12. `nmap -sX Target` (sends FIN, PSH, URG) (if no response the port is open)
13. `nmap -PR Target` (does ARP scan. Add `-sn` if port scanning isn’t needed)
14. `nmap -S SPOOFED_IP MACHINE_IP` (sends spoofed ip address)
15. `nmap -PE Target` (to send icmp echoe request to all hosts in the target network. It’ll be blocked by firewalls mostly cuz of built-in firewall in MS Windows)

## Google dorking:

Use nasa.gov as example.

1. `site:nasa.gov` gives only results with nasa.gov
2. `site:nasa.gov intitle:home` gives result with ‘home’ in title of the search result.
3. `site:nasa.gov intext:username` gives search result where desc (under the title) has the word “username”.
4. `site:nasa filetype:pdf` show results with pdf files.
5. `site:nasa filetype:pdf inurl:mars.nasa,gov` excludes the specific url mentioned (`mars.nasa.gov`).

---

### Use google dorking cheatsheet for all the dorking commands:

Github link: [Google Dorking](https://gist.github.com/sundowndev/283efaddbcf896ab405488330d1bbc06)
Cheatsheet: [3eye](https://3eye.vercel.app/)

