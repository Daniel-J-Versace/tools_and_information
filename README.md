# tools_and_information
A page for tools and information on information security and cyber

## CEH Tools
### Scanning and Enumeration
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

Website Mirroring & Email footprinting
- https://httrack.com HTTrack copies websites
- https://softbytelabs.com/wp/blackwidow/ again copies websites
- https://webripper.software.informer.com/2.0/ rips images and files from URLs
- https://teleport-pro.en.softonic.com/?ex=RAMP-3864.5&rex=true very old piece of software, but looks to make copies of sites
- https://www.gnu.org/software/wget/ Wget retrieves files from HTTP/s FTP and more.
- https://github.com/Security-Tools-Alliance/Infoga email OSINT
- https://politemail.com/ 
- https://emailtracker.website/pro

DNS and Whois Footprinting
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

Next bits are for "Competitive intelligence"
- EDGAR DB (https://www.sec.gov/search-filings)
- LexisNexis
DB & Hoovers





### Sniffing and Evasion


### Attacking a System


### Web-based Hacking: Servers and apps


### Wireless Network Hacking


### Mobile Communications and IoT


### Security in Cloud Computing


### Trojans and Other Attacks


### Cryptography


### Low tech: Social Eng and Physical Security


### Artificial Intelligence for hacking


### Pentesting
