---
layout: default
title: 1
permalink: /passiverecon
---

<details>
  <summary><strong> DOMAIN OR IP ADDRESS PASSIVE RECON </strong></summary>
  
Records and properties:
* [ ] Find domain's owner, registrar and contacts informations - Service : who.is
* [ ] Find IP, domains, subdomains records for target  - Tool : dig

Subdomain discovery :
* [ ] Discover potential subdomains - Tool : subfinder
* [ ] Discover referenced subdomains - Google dork : "site:\*.domain.com -site:www.domain.com"

Services discovery :
* [ ] Discover exposed services for a domain name or IP - Service : shodan.io

</details>

**------------ DOMAIN OR IP ADDRESS PASSIVE RECON ------------**

Records and properties:
* [ ] Find domain's owner, registrar and contacts informations - Service : who.is
* [ ] Find IP, domains, subdomains records for target  - Tool : dig

Subdomain discovery :
* [ ] Discover potential subdomains - Tool : subfinder
* [ ] Discover referenced subdomains - Google dork : "site:\*.domain.com -site:www.domain.com"

Services discovery :
* [ ] Discover exposed services for a domain name or IP - Service : shodan.io

**------------ WEB APPLICATION PASSIVE RECON ------------**

**ZERO-TOUCH**

Technology discovery :
- [ ] Discover underlying technologies for a web application - Tool : Wappalyzer

Audit SSL/TLS :
- [ ] Discover SSL/TLS configuration, version and used cyphersuites - Service : ssltest

Audit HTTP :
- [ ] Discover HTTP version and headers - Service : securityheaders.com

Endpoints discovery :
- [ ] Discover endpoints and URLs for a web application or domain - Tool : GetAllURLs

Zero-touch crawling :
* [ ] Manually crawl the web application - Tool : BurpSuite and it's proxy enabled with the "JSLinkFinder" extension activated.

**LIGHT-TOUCH**

Light-touch crawling :
* [ ] Manually crawl through previous web application versions and pages - Service : Waybackmachine.

Public files :
* [ ] Scrape robots.txt
* [ ] Scrape sitemap.xml and sitemap files
* [ ] Search for .txt files - Google dork : 'site:$TARGET filetype:txt'
* [ ] Search for .env files - Google dork : 'site:$TARGET filetype:env'
* [ ] Search for .log files - Google dork : 'site:$TARGET filetype:log'
* [ ] Search for .old files - Google dork : 'site:$TARGET filetype:old'
* [ ] Search for .bak files - Google dork : 'site:$TARGET filetype:bak'
* [ ] Search for .docx files - Google dork : 'site:$TARGET filetype:docx'
* [ ] Search for .xlsx files - Google dork : 'site:$TARGET filetype:xlsx'
* [ ] Search for .pdf files - Google dork : 'site:$TARGET filetype:pdf'
* [ ] Search for .xml files - Google dork : 'site:$TARGET filetype:xml'
* [ ] Search for .json files - Google dork : 'site:$TARGET filetype:json'

Interesting endpoints :
* [ ] Search for .git endpoints - Google dork : 'site:$TARGET ".git"'
* [ ] Search for index endpoints - Google dork : 'site:$TARGET intitle:"Index of"'