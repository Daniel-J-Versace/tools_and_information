# tools_and_information
A page for tools and information on information security and cyber

# CEH Tools
## Scanning and Enumeration
- https://www.exploit-db.com/google-hacking-database Google hacking database. Examples on how to manipulate search strings.

|  Operator  | Syntax | Description |
|------------|--------|--------------------------------------------------------------------|
| filetype | **filetype:** `type` | Searches only for files of a specific type. |
| index of | **index of** `/string` | Displays pages with directory browsing enabled, use with another operator. E.g., `"intitle:index of" passwd` will show dr listings containing passwd. |
| info | **info:** `string` | Displays information Google stores about the page itself. `info:www.bbc.co.uk`. |
| intitle | **intitle:** `string` | Searches for pages that contain the string in the title. `intitle:login` or for multiple strings `allintitle:login pass word`. |
| inurl | **inurl:** `string` | Displays pages with the string in the URL. e.g., `inurl:passwd` will display all pages with the word passwd in the URL. Multiple Strings use `allinurl` so `allinurl:etc passwd`. |
| link | **link:** `string` | Displays linked pages based on a search term. |
| related | **related:** `webpage name` | Shows web pages similar to the webpage name. |
| cache | **cache:** `https://example.com/page.html` | Shows the cached version of a page. |
| site | **site:** `domain or wep page string` | Displays pages for a specific website or domain holding the search term. e.g., `site:anywhere.com passwds` will display all pages with the text `passwds` within the site `anywhere.com`. |

- https://Shodan.io Goes without saying.
- The Harvester (https://www.kali.org/tools/theharvester/) repo (https://github.com/laramies/theHarvester). OSINT for emails, IPs, Names, URLSs and more.
- https://trends.google.com/trends/
- https://www.hashatit.com/ (seems to be down)
- http://archive.org is the Wayback Machine URL

### Website Mirroring & Email Footprinting
- https://httrack.com HTTrack copies websites
- https://softbytelabs.com/wp/blackwidow/ again copies websites
- https://webripper.software.informer.com/2.0/ rips images and files from URLs
- https://teleport-pro.en.softonic.com/?ex=RAMP-3864.5&rex=true very old piece of software, but looks to make copies of sites
- https://www.gnu.org/software/wget/ Wget retrieves files from HTTP/s FTP and more.
- https://github.com/Security-Tools-Alliance/Infoga email OSINT
- https://politemail.com/ 
- https://emailtracker.website/pro
- Burp Suite
- Firebug
- Website informer

### DNS and Whois Footprinting
- https://www.iana.org/domains/root/servers Internet Assigned Numbers Authority and the Root Servers list.

|  DNS Record Type | Label | Description |
|-----|--------|--------------------------------------------------------------------|
| SRV | Service | Defines the hostname and port number of servers providing specific services such as directory services server. |
| SOA | Start of Authority | Identifies the primary name server for the zone. The SOZ record contains the hostname of the server responsible for all DNS records within the namespace as well as basic properties of the domain. |
| PTR | Pointer | This maps an IP address to a hostname (provides reverse DNS lookups). Not absolutely needed for every entry in your DNS namespace, but are usually associated with email server records. |
| NS | Name Server | The record defines the name servers within your namespace. These are the ones that respond to clients' requests for name resolution. |
| MX | Mail Exchange | Identifies email servers within a domain. |
| CNAME | Canonical Name | Provides for domain name aliases within your zone. E.g., If an FTP service and a web service are running on the same IP. CNAME could be used to list both within DNS. |
| A | Address | Maps an IP to hostname.

- https://whois.domaintools.com/ 
- `nslookup` is used to query DNS servers for information.
- `dig` test DNS queries and get results.

### Network Footprinting
- `traceroute` or `tracert` tracks packets across the net providing transit times and paths.


Next bits are for "Competitive intelligence"
- EDGAR DB (https://www.sec.gov/search-filings)
- https://www.geeksforgeeks.org/linux-unix/osrframework-open-source-research-framework-on-linux/ 
- LexisNexis
- DB & Hoovers

### TCP/IP Networking
### Flags
SYN (*Synchronize*)
    This flag is set when establishing the communication, during which it negotiations parameters and sequence numbers.

ACK (*Acknowledgement*)
    Set as a response to SYN flags, will be set on all segments after the initial SYN flag.

RST (*Reset*)
    Forces termination of communications in both directions.

FIN (*Finish*)
    Orders a close to communications.

PSH (*Push*)
    Forces delivery of data without concern for buffering, so the device receiving doesn't need to wait for the buffer to fill up before it processes the data.

URG (*Urgent*)
    Signifies the data being sent is out of band, cancelling a message midstream for example.

### Packet Crafting tools
- https://www.netscantools.com/nstbasicmain.html NetScanTools - Network tools such as DNS, IP/Hostname resolution, Who Am I, Ping (and graphical) Traceroute.
- https://ostinato.org/ Ostinato - packet generator, generate, customise and replay L2/L3 traffic.
- https://packeth.sourceforge.net/packeth/Home.html PackETH - An ethernet packet generator, GUI and CLI tool to send any possible packet or sequence.
- https://candelatech.com/ LANforge FIRE - Looks like a whole suite of Network testing tools, including WiFi traffic generator.
- https://www.colasoft.com/download/products/download_packet_builder.php Colasoft Packet Builder - packet builder allows HEX editing of RAW data and a decoding editor.

### Ports
- https://www.nirsoft.net/utils/cports.html CurrPorts - Network monitoring software to display open ports (TCP/IP & UDP) including things like what process opened it, time and user.

- **Well-known Ports**  0-1023
- **Registered Ports** 1024-49,151
- **Dynamic Ports** 49,152-65,535 

| Port Number | Protocol | Transport Protocol |
|-------------|----------|--------------------|
|**20/21**| *FTP* | TCP |
|**22**| *SSH* | TPC |
|**23** | *Telnet* | TCP |
| **25**| *SMTP* | TCP |
|**53**| *DNS* | TCP & UDP|
|**67**| *DHCP* | UDP | 
|**69**| *TFTP* | UDP |
|**80**| *HTTP* | TCP |
|**88**| *Kerberos* | TCP |
|**110**| *POP3* | TCP |
|**123**| *NTP* | UDP | 
|**135**| *RPC* | TCP |
|**137-139**| *NetBIOS* | TCP & UDP |
|**143**| *IMAP* | TCP |
|**161/162**| *SNMP* | UDP |
|**179**| *BGP* | TCP |
|**389**| *LDAP* | TCP & UDP |
|**443**| *HTTPS* | TCP |
|**445**| *SMB* | TCP |
|**514**| * Syslog* | UDP |
|**631**| * IPP* | TCP |
|**500**| *IKE/VPN* | UDP |

### Subnetting
TBC 

### ICMP
ICMP message types. 

| ICMP Message type | Description and important codes |
|-------------------|---------------------------------|
| 0: Echo Reply | Answer to a Type 8 Echo Request |
| 3: Destination<br>Unreachable | Error message indicating the host or network cannot be reached. The codes are: <br>**0**-Destination network unreachable <br>**1**-Destination host unreachable <br>**6**-Network unknown <br>**7**-Host unknown <br>**9**-Network administratively prohibited <br>**10**-Host administratively prohibited <br>**13**-Communication administratively prohibited |
| 4: Source Quench | A congestion control message |
| 5: Redirect | Sent when there are two or more gateways available for the sender to use and the best route available to the destination is not the configured default gateway. Codes are: <br>0-Redirect datagram fro the network <br>1-Redirect datagram for the host |
|8: Echo Request | A ping message requesting an Echo Reply |
|11: Time exceeded | Message indicating that the packet took too long to be routed to the destination (code 0 is TTL expired) |


## Sniffing and Evasion


## Attacking a System


## Web-based Hacking: Servers and apps


## Wireless Network Hacking


## Mobile Communications and IoT


## Security in Cloud Computing


## Trojans and Other Attacks


## Cryptography


## Low tech: Social Eng and Physical Security


## Artificial Intelligence for hacking


## Pentesting
