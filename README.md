# Webrecon
Materiais e tools para web recon.

## Subdomain discovery
### Historic
* securitytrails.com
* subdomainfinder.cc99.nl
* web.archive.org
* dnsdumpster.com
* https://github.com/screetsec/sudomy

### Brute Force
* https://github.com/aboul3la/sublist3r
* https://github.com/therook/subbrute
* https://github.com/OWASP/amass

### Certificates, passive
* https://github.com/projectdiscovery/subfinder
* sslmate.com/certspotter
* https://github.com/unapibageek/ctfr (Uses crt.sh)
* chaos.rpojectdiscovery.io

## Application discovery
### Url Discovery
* https://github.com/lc/gau
* https://github.com/hakluke/hakrawler
* https://github.com/xmendez/wfuzz
* https://github.com/ffuf/ffuf
* https://github.com/maurosoria/dirsearch

### Parameter discovery
* https://github.com/devanshbatham/paramspider
* https://github.com/tomnomnom/gf
* https://github.com/s0md3v/Parth
* https://github.com/tomnomnom/hacks/tree/master/kss

### Content discovery
* https://github.com/projectdiscovery/httpx
* https://github.com/michenriksen/aquatone
* https://github.com/m4ll0k/SecretFinder

## Fuzzing
* https://github.com/xmendez/wfuzz
* https://github.com/ffuf/ffuf

<p>Fuzzing of directories and file <br>
We can use the seclists -> discovery lists to fuzz for directories and files. Examples of lists: big, common, raft and specifics for webservers and apps.<br>
wfuzz commands:<br>
-c for colourfull<br>
-z for range fuzz or file fuzz<br>
--hc 404 hides the http 404 response code (better to use --hc 404 then --sc 200 for it show other status codes such as 300 and 500)<br>
-t number of threads
the tool will replace de word "FUZZ" for the contents of the list </p>

> wfuzz -t 10 -c -z file,common.txt --hc 404 http://[ip or host]/FUZZ
