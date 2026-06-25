# Cybersecurity Training Notes – June 2026

## OSINT

### 1. Find location (coordinates), restaurant name and exact location in street view map.

#### Steps:

1. Use Yandex image search (Rus and Euro based results) and find exact or similar images.
2. Take hints from visible shop names and search for it in the maps.
3. Use street view in maps and navigate to the exact location where the picture was taken.

### 2. Find exact location from a picture presented with captions and hint.

#### Steps:

1. Gather hints from the picture like billboard and find an approximate location.
2. Look up the event info and search for starting point of the event.
3. Look for the exact location using Google street view in the map.

#### OSINT Tools

* Pic2map – used to find location if a picture
* Exiftool – linux
* Jimpl.com – website for exif
* Flightradar24 to find details about flights
* Marinetraffic to gather details about ships

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
16. `nmap -sV <target>` shows the version of the services
17. `nmap -O <target>` shows the operating system of the server
18. `nmap -p- <target>` scans all 65535 ports
19. `nmap -T5 <target>` fast an noisy (fast)
20. `nmap -T0 <target>` sneaky scan (slow)

Try this:

```bash
nmap -p- -sV -O -T5 <ip>
```

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

---

## Gobuster

Used to capture various endpoints in a webpage

```bash
gobuster dir -u <url> -w </path/to/wordlist.txt>
```

If needed to discover what are the files present

```bash
gobuster dir -u <url> -x <extensions> -w </path/to/wordlist.txt>
```

---

## Steganography (Image analysis)

### Basic Steganography Tools

1. Analyze the file type of the image `file <filename.ex>`
2. Check Metadata of the image `exiftool <filename.ex>`
3. Check strings of the image `strings <filename.ex>`
4. Use binwalk to analyze extract hidden files `binwalk <filename.ex>`
5. Extract data using Steghide `steghide extract -sf <filename.ex>`
6. Use outguess to extract text file `outguess -r <filename.ex> <output.txt>`



## TryHackMe Rooms
* [ ] [Ohsint](https://tryhackme.com/room/ohsint/)
* [ ] [Sakura](https://tryhackme.com/room/sakura/)
* [ ] [SearchLight](https://tryhackme.com/room/searchlightosint/)
* [ ] [Kenobi](https://tryhackme.com/room/kenobi/)
* [ ] [Vulnversity](https://tryhackme.com/room/vulnversity/)
* [ ] [Blue](https://tryhackme.com/room/blue/)
* [ ] [Ice](https://tryhackme.com/room/ice/)
* [ ] [PickleRick](https://tryhackme.com/room/picklerick/)
* [ ] [Wgel CTF](https://tryhackme.com/room/wgelctf/)
* [ ] [Crack The Hash](https://tryhackme.com/room/crackthehash/)
* [ ] [c4ptur3-th3-fl4g](https://tryhackme.com/room/c4ptur3th3fl4g/)
* [ ] [Bolt](https://tryhackme.com/room/bolt/)
* [ ] [Cicada-3301 Vol:1](https://tryhackme.com/room/cicada3301vol1/)
* [ ] [Basic Pentesting](https://tryhackme.com/room/basicpentestingjt/)
* [ ] [Lian Yu](https://tryhackme.com/room/lianyu/)
