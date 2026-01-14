---
layout: default
title: Passive recon checklist
permalink: /passive_recon_checklist
---

<details>
	<summary><span style="color:#2ecc71;"><strong> DOMAIN OR IP ADDRESS PASSIVE RECON </strong></span></summary>
		<hr>
		<strong> Records and properties: </strong>
		<ul>
		<li> [ ] Find domain's owner, registrar and contacts informations - Service : who.is </li>
		<li> [ ] Find IP, domains, subdomains records for target  - Tool : dig </li>
		</ul>
		<strong> Subdomain discovery : </strong>
		<ul>
		<li> [ ] Discover potential subdomains - Tool : subfinder </li>
		<li> [ ] Discover referenced subdomains - Google dork : "site:\*.domain.com -site:www.domain.com" </li>
		</ul>
		<strong> Services discovery : </strong>
		<ul>
		<li> [ ] Discover exposed services for a domain name or IP - Service : shodan.io </li>
		</ul>
</details>
<hr>
<details>
	<summary><span style="color:#3498db;"><strong> WEB APPLICATION PASSIVE RECON </strong></span></summary>
	<hr>
	<details>
		<summary><strong> ZERO-TOUCH </strong></summary>
		<hr>
		<strong> Technology discovery : </strong>
		<ul>			<li> [ ] Discover underlying technologies for a web application - Tool : Wappalyzer </li>
		</ul>
		<strong> Audit SSL/TLS : </strong>
		<ul>
		<li> [ ] Discover SSL/TLS configuration, version and used cyphersuites - Service : ssltest </li>
		</ul>
		<strong> Audit HTTP : </strong>
		<ul>
		<li> [ ] Discover HTTP version and headers - Service : securityheaders.com </li>
		</ul>
		<strong> Endpoints discovery : </strong>
		<ul>
		<li> [ ] Discover endpoints and URLs for a web application or domain - Tool : GetAllURLs </li>
		</ul>
		<strong> Crawling : </strong>
		<ul>
		<li> [ ] Manually crawl the web application - Tool : BurpSuite and it's proxy enabled with the "JSLinkFinder" extension activated. </li>
		</ul>
	</details>
	<details>
		<summary><strong> LIGHT-TOUCH </strong></summary>
		<hr>
		<strong> Crawling : </strong>
		<ul>
		<li> [ ] Manually crawl through previous web application versions and pages - Service : Waybackmachine. </li>
		</ul>
		<strong> Public files : </strong>
		<ul>
		<li> [ ] Scrape robots.txt </li>
		<li> [ ] Scrape sitemap.xml and sitemap files </li>
		<li> [ ] Search for .txt files - Google dork : 'site:$TARGET filetype:txt' </li>
		<li> [ ] Search for .env files - Google dork : 'site:$TARGET filetype:env' </li>
		<li> [ ] Search for .log files - Google dork : 'site:$TARGET filetype:log' </li>
		<li> [ ] Search for .old files - Google dork : 'site:$TARGET filetype:old' </li>
		<li> [ ] Search for .bak files - Google dork : 'site:$TARGET filetype:bak' </li>
		<li> [ ] Search for .docx files - Google dork : 'site:$TARGET filetype:docx' </li>
		<li> [ ] Search for .xlsx files - Google dork : 'site:$TARGET filetype:xlsx' </li>
		<li> [ ] Search for .pdf files - Google dork : 'site:$TARGET filetype:pdf' </li>
		<li> [ ] Search for .xml files - Google dork : 'site:$TARGET filetype:xml' </li>
		<li> [ ] Search for .json files - Google dork : 'site:$TARGET filetype:json' </li>
		</ul>
		<strong> Interesting endpoints : </strong>
		<ul>
		<li> [ ] Search for .git endpoints - Google dork : 'site:$TARGET ".git"' </li>
		<li> [ ] Search for index endpoints - Google dork : 'site:$TARGET intitle:"Index of"' </li>
		</ul>
	</details>
</details>












