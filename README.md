<div align="center">

<h1>PENETRATION TESTING REPORT</h1>

<h2>FOOTPRINTING, PASSIVE RECONNAISSANCE & NETWORK SCANNING</h2>

<h3>W2-PM1 | W2-PM2 | W2-PM3 | W2-PM4 | W2-PM5 | CYBERSECURITY | NETWORKWALKS</h3>
<h3>W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS</h3>

<br>

<img src="https://img.shields.io/badge/Status-Completed-brightgreen">
<img src="https://img.shields.io/badge/Program-Networkwalks-0099cc">
<img src="https://img.shields.io/badge/Week-02-blue">

<br>

<img src="https://img.shields.io/badge/Modules-5-blue">
<img src="https://img.shields.io/badge/Type-Pentest%20Report-red">

<br>

<img src="https://img.shields.io/badge/Tool-Kali%20Linux-blue">
<img src="https://img.shields.io/badge/Tool-Maltego-orange">
<img src="https://img.shields.io/badge/Tool-Zenmap-yellow">

<br>

<img src="https://img.shields.io/badge/Format-Markdown-lightgrey">
<img src="https://img.shields.io/badge/Platform-GitHub-black">
<img src="https://img.shields.io/badge/License-Educational%20Use%20Only-purple">

</div>

<table>
  <tr>
    <td align="center"><b>Pentester Name<br>(Cybersecurity Trainee)</b></td>
    <td><b>Jenik Shrestha</b></td>
  </tr>

  <tr>
    <td align="center"><b>Program/Batch</b></td>
    <td>B082-Networkwalks</td>
  </tr>

  <tr>
    <td align="center"><b>Date</b></td>
    <td>20 August 2026</td>
  </tr>

  <tr>
    <td align="center"><b>Modules Completed</b></td>
    <td>
      W2-PM1 – Footprinting & Reconnaissance with Multiple Kali Tools<br>
      W2-PM2 – Footprinting with GHDB (Google Hacking Database)<br>
      W2-PM3 – Footprinting with Maltego<br>
      W2-PM4 – Footprinting & Reconnaissance with theHarvester<br>
      W2-PM5 – Network Scanning with Zenmap
    </td>
  </tr>

  <tr>
    <td align="center"><b>Client/Target</b></td>
    <td>
      1. networkwalks.com – Authorized educational target<br>
      2. microsoft.com – Passive reconnaissance using public sources<br>
      3. Google Search (GHDB) – Exposed open directories and cameras<br>
      4. My own local LAN network – 192.168.18.0/24
    </td>
  </tr>

  <tr>
    <td align="center"><b>Permission secured?</b></td>
    <td>Yes – All activities were performed within an authorized educational scope or on my own local network. (See Section 9 for the Authorization Letter).</td>
  </tr>

  <tr>
  <td align="center"><b>Phases Covered</b></td>
  <td>
    <b>Phase 1:</b> Reconnaissance & Footprinting – W2-PM1 (whois, whatweb, nslookup, curl, wafw0f, dnsrecon)<br>
    <b>Phase 2:</b> Open Source Intelligence (OSINT) – W2-PM2 (GHDB / Google Dorking)<br>
    <b>Phase 3:</b> Graphical OSINT & Footprinting – W2-PM3 (Maltego)<br>
    <b>Phase 4:</b> Passive Email & Subdomain Harvesting – W2-PM4 (theHarvester)<br>
    <b>Phase 5:</b> Network Scanning & Discovery – W2-PM5 (Zenmap)<br>
    <b>Phase 6:</b> In Progress
  </td>
</tr>
</table>

## 1. Liability Disclaimer

All activities documented in this report were performed strictly for **educational and cybersecurity research purposes**.

The **Footprinting & Reconnaissance with Multiple Kali Tools (W2-PM1)**, and **Footprinting with Maltego (W2-PM3)** activities were conducted against `networkwalks.com` within the scope of the assigned cybersecurity training environment.

The **Footprinting with GHDB (W2-PM2)** activities were conducted solely to search for publicly indexed open directories and exposed cameras for educational awareness. No exploitation or unauthorized access was attempted.

The **Footprinting & Reconnaissance with theHarvester (W2-PM4)** activity was performed against `microsoft.com` using publicly available information sources as part of a **passive reconnaissance exercise**. No attempt was made to gain unauthorized access, bypass security controls, or modify any data.

The **Network Scanning with Zenmap (W2-PM5)** activities were performed only on **my own local LAN network and devices under my control**.

No unauthorized access, exploitation, or modification of systems was performed during these exercises.

> **⚠️ Important:** The tools and techniques demonstrated in this report must only be used for legitimate educational, research, and authorized security testing purposes. Unauthorized access, scanning, exploitation, or misuse may violate applicable laws and regulations.

All activities were completed as part of assigned cybersecurity training exercises. Any misuse of the techniques described in this report is the sole responsibility of the individual performing such actions.

## 2. Introduction

This report documents five practical cybersecurity activities completed as part of the Week 2 project modules: **Footprinting & Reconnaissance with Multiple Kali Tools (W2-PM1)**, **Footprinting with GHDB (W2-PM2)**, **Footprinting with Maltego (W2-PM3)**, **Footprinting & Reconnaissance with theHarvester (W2-PM4)**, and **Network Scanning with Zenmap (W2-PM5)**.

The first, third, and fourth activities focused on gathering publicly available information about `networkwalks.com` and `microsoft.com` using **WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, DNSRecon, Maltego, and theHarvester**. These tools were used to identify domain registration details, web technologies, IP addresses, HTTP response headers, WAF detection, DNS records, emails, and subdomains.

The second activity involved using **Google Hacking Database (GHDB)** dorks to discover publicly exposed resources like live security cameras and unsecured PDF directories on the internet.

The fifth activity focused on **local network discovery using Zenmap**, the graphical interface for Nmap. My local IP address and LAN subnet were identified, followed by a Ping Scan of the `192.168.18.0/24` network. The scan identified active hosts, their IP and MAC addresses, and a visual network topology was generated.

All activities were performed within an authorized educational scope. The purpose of these exercises was to understand how reconnaissance, OSINT, and network scanning techniques can be used to gather information about systems and networks during the initial stages of a penetration test.

## 3. Tools Used

The table below lists each tool used in this report and its purpose.

| **Tool** | **Purpose** |
|---|---|
| **Kali Linux** | Operating system used to perform the footprinting and reconnaissance activities. |
| **WHOIS** | Used to obtain domain registration details such as registrar information, registration dates, and name servers. |
| **WhatWeb** | Used to fingerprint web technologies such as the web server, CMS, plugins, frameworks, and IP address. |
| **Nslookup** | Used to resolve a domain name to its corresponding IP address using DNS. |
| **Curl (`curl -I`)** | Used to inspect HTTP response headers and identify technical information exposed by the web server. |
| **Wafw00f** | Used to detect whether the target website is protected by a Web Application Firewall (WAF). |
| **DNSRecon** | Used to enumerate DNS records such as NS, MX, TXT, SPF, SRV, and other DNS-related information. |
| **Google Hacking Database (GHDB)** | Used to find Google Dorks for searching exposed cameras, config files, and open directories via Google. |
| **Maltego** | Used for graphical OSINT (Open Source Intelligence) to visualize and find email addresses related to a domain. |
| **theHarvester** | Used for passive reconnaissance to collect publicly available information such as email addresses, hosts, and subdomains related to a target organization from various search engines. |
| **Windows** | Operating system used for the local network scanning activity with Zenmap. |
| **Windows CMD / Terminal** | Used to identify the local IP address, subnet mask, default gateway, and MAC address using commands such as `ip addr` and `ipconfig`. |
| **Zenmap** | Graphical user interface for Nmap used to scan the local LAN subnet, discover active hosts, identify IP and MAC addresses, and generate a network topology. |
| **Nmap** | Network scanning engine used by Zenmap to perform host discovery and Ping Scan operations on the local network. |

## 4. Activities Performed

### 4.1 Footprinting & Reconnaissance (W2-PM1)

I performed footprinting and reconnaissance activities against `networkwalks.com` using multiple Kali Linux tools. The objective was to collect publicly available technical information about the target and understand its external infrastructure.

The following tools were used:

- **WHOIS** – revealed the registrar, registration and expiry dates (2027-11-07), and HostGator name servers.
- **WhatWeb** – identified the web server as **Apache**, the CMS as **WordPress 7.0.4**, the server IP `192.232.216.135`, and an email address `info@networkwalks.com`.
- **Nslookup** – resolved the domain `networkwalks.com` to `192.232.216.135`.
- **Curl (`curl -I`)** – returned an **HTTP/2 200** response and exposed technical information related to the web server, nginx cache, and WordPress REST API endpoints.
- **Wafw00f** – successfully identified **ModSecurity (SpiderLabs)** Web Application Firewall protecting the website.
- **DNSRecon** – enumerated the target's DNS infrastructure, including name servers, A records, MX records for mail servers, TXT/SPF records, and various SRV records.

### 4.2 Footprinting with GHDB (W2-PM2)

I utilized the **Google Hacking Database (GHDB)** hosted on `exploit-db.com` to uncover publicly exposed devices and files on the internet using advanced Google search queries (Google Dorks).

- **Task 1 (Security Cameras):** I searched for live exposed security cameras using the dork `intitle:"webcamXP" inurl:8080` and others, identifying active unprotected camera feeds, such as `http://122.116.41.8:8080`.
- **Task 2 (Math Ebooks):** I found open directories containing downloadable PDF math ebooks using the dork `intitle:index.of "parent directory" mathematics pdf`. Several results, such as those found at `skylineuniversity.ac.ae`, were verified to contain publicly accessible academic files.

This activity demonstrated how easily attackers can leverage Google's indexing power to find exposed internal resources and unsecured hardware.

### 4.3 Footprinting with Maltego (W2-PM3)

I installed and configured **Maltego** on a Windows PC to perform visual OSINT discovery against `networkwalks.com`.

The steps performed included:
1.  Successfully installed and activated Maltego via the provided setup file.
2.  Created a new graph and added a **Domain** entity.
3.  Double-clicked the entity and set the target domain to `networkwalks.com`.
4.  Ran the **Email Addresses from Domain** transform.
5.  Maltego successfully queried public sources and harvested `info@networkwalks.com` as a publicly available email address. The visual graph clearly showed the relation between the domain and the discovered email.

### 4.4 Passive Reconnaissance with theHarvester (W2-PM4)

I performed passive reconnaissance against `microsoft.com` using **theHarvester** in Kali Linux to gather publicly available information without directly interacting with the target.

- For the first task, I used **Baidu** as the data source and set the maximum number of results to 1000: `theHarvester -d microsoft.com -l 1000 -b baidu`.
  - This operation successfully identified **4 emails** and **22 hosts** related to `microsoft.com`.
- For the second task, I used all supported sources (`-b all`) and limited the results to 50: `theHarvester -d microsoft.com -l 50 -b all`.
  - This execution revealed that many public sources require API keys, causing some failed searches, but it demonstrated how aggressive querying can yield richer, more granular OSINT data.

### 4.5 Network Scanning with Zenmap (W2-PM5)

For the network scanning activity, I used **Zenmap**, the graphical interface for Nmap, to perform host discovery on my own local LAN network.

- First, I identified my local network configuration via the `ip addr` command in Kali: `192.168.18.219`.
- The subnet `192.168.18.0/24` was entered as the target.
- A Ping Scan (`-sn` profile) was performed using `nmap -sn 192.168.18.0/24`.
- The scan identified **multiple live hosts** on the network, including `192.168.18.1` (dev.opt), `192.168.18.13`, `192.168.18.76`, `192.168.18.219` (own PC), etc.
- I identified MAC addresses associated with these IPs (e.g., `20:D2:76:4B:1E:3C`, `04:BA:8D:BD:C8:EF`, `4C:F2:02:05:19:2F`).
- Finally, I opened the **Topology** section to generate a visual "Fisheye" map of the network and saved it as a PDF document.

## 5. Risk Analysis / Impact

Based on the information collected during the **footprinting, passive reconnaissance, GHDB, and network scanning activities**, the following potential security risks and observations were identified.

| # | **Risk / Finding**                                    | **Evidence / Observation**                                                                                                    | **Potential Impact**                                                                                                                                     | **Risk Level** |
| - | ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| 1 | Public domain and infrastructure information exposed  | WHOIS revealed registrar details, registration dates, and HostGator name servers for `networkwalks.com`.                      | Public infrastructure information can assist attackers in building a detailed profile of the target during reconnaissance.                               | 🟡 Low         |
| 2 | Server IP address identifiable                        | Nslookup resolved `networkwalks.com` to `192.232.216.135`.                                                                    | The public server IP can be used to map the target's infrastructure and support further authorized enumeration.                                          | 🟡 Low         |
| 3 | HTTP technical information exposed                    | `curl -I` returned HTTP headers showing **Apache**, WordPress-related information, cookies, and the `/wp-json/` API endpoint. | Technical information may help an attacker fingerprint the web application and identify additional areas for investigation.                              | 🟡 Low         |
| 4 | WAF technology identifiable                           | Wafw00f identified **ModSecurity (SpiderLabs)** protecting `networkwalks.com`.                                                | Identifying the WAF reveals information about the website's defensive architecture and may help an attacker adapt later reconnaissance attempts.         | 🟡 Low         |
| 5 | Public email addresses discoverable                   | Maltego and theHarvester successfully harvested `info@networkwalks.com` and emails from `microsoft.com`.                      | Publicly available email addresses may be used in phishing, social engineering, or credential-targeting campaigns.                                       | 🟠 Medium      |
| 6 | Unsecured IP Cameras exposed online                   | GHDB queries revealed live IP camera feeds (`webcamXP`) accessible via public IP addresses like `122.116.41.8:8080`.          | Exposed IoT devices are vulnerable to unauthorized viewing, and can serve as entry points into the local network (if not isolated).                     | 🔴 Critical    |
| 7 | Public open directories with sensitive PDFs           | GHDB queries found open directories (`intitle:index.of`) containing academic/math PDFs.                                       | Unrestricted access to sensitive files can lead to intellectual property theft or further targeted attacks.                                              | 🟠 Medium      |
| 8 | Multiple active hosts discovered on the local network | Zenmap identified **numerous live hosts** on the `192.168.18.0/24` subnet (including `192.168.18.1`, `.13`, `.76`).           | Network discovery can reveal active devices and network structure. Unexpected devices should be verified by the network owner.                           | 🟠 Medium      |
| 9 | MAC address information discoverable                  | Zenmap and `ip addr` identified MAC addresses associated with specific devices (Huawei, Samsung, Xiaomi).                     | MAC address information can help identify devices and network hardware during internal reconnaissance.                                                   | 🟡 Low         |

**Risk Level Key:** 🔴 Critical | 🟠 Medium | 🟡 Low

> **Note:** The findings above are reconnaissance, OSINT, and network-discovery observations and should not automatically be considered confirmed vulnerabilities. No exploitation or vulnerability validation was performed during these project modules.

## 6. Recommendations

Based on the observations from the **footprinting, passive reconnaissance, Google Dorking, and network scanning activities**, the following security recommendations are suggested:

1. **Review Publicly Exposed Information**  
   Organizations should regularly review what information about their domains, servers, technologies, and infrastructure is publicly accessible to search engines.

2. **Keep Web Technologies Updated**  
   Web servers, CMS platforms, plugins, and other technologies should be regularly updated and checked against current security advisories.

3. **Review HTTP Response Headers**  
   HTTP headers should be reviewed to ensure that unnecessary technical information about the server, framework, or application is not being exposed.

4. **Reduce Unnecessary Public Email Exposure**  
   Organizations should monitor publicly available email addresses because exposed addresses may become targets for phishing and social engineering attacks.

5. **Secure and Isolate IoT Devices**  
   Security cameras and other IoT devices must be properly configured, use strong default password changes, and should ideally be placed on isolated VLANs. They should never be exposed directly to the public internet without proper authentication mechanisms.

6. **Prevent Directory Indexing and Exposed Files**  
   Web servers and FTP servers should have directory indexing disabled to prevent Google from publicly indexing open folders. Sensitive files (PDFs, configuration files, backups) should be stored outside the web root.

7. **Review DNS Records Regularly**  
   DNS records such as NS, MX, TXT, SPF, and SRV records should be periodically reviewed to ensure that only necessary information and services are publicly exposed.

8. **Monitor Public Subdomains and Hosts**  
   Publicly discoverable subdomains and hosts should be regularly inventoried and reviewed. Unused or outdated services should be removed or secured to reduce the external attack surface.

9. **Perform Regular Internal Network Discovery**  
   Organizations should periodically scan their own authorized networks to identify active devices and maintain awareness of systems connected to the network.

10. **Investigate Unknown Devices**  
    Any unexpected or unauthorized device discovered during internal network scanning should be identified and investigated.

11. **Maintain Updated Network Documentation**  
    IP addresses, MAC addresses, devices, network topology, and other infrastructure information should be documented and kept up to date.

12. **Perform Security Testing Only with Authorization**  
    Reconnaissance, scanning, and other cybersecurity testing activities should only be performed against systems and networks where proper authorization and an agreed scope have been established.

## 7. Conclusion

During the Week 2 cybersecurity project activities, I completed practical exercises covering **footprinting, reconnaissance, Google dorking, passive information gathering, and local network scanning**.

In the **W2-PM1 Footprinting & Reconnaissance** activity, I used multiple Kali Linux tools including **WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon** to collect publicly available information about `networkwalks.com`. These tools helped identify domain registration details, web technologies, IP information, HTTP response headers, WAF, and DNS records.

In the **W2-PM2 GHDB** activity, I utilized Google Dorks to safely discover exposed internet-facing IP cameras and open directories containing PDF resources, highlighting the widespread issue of unintentional information leakage through search engine indexing.

In the **W2-PM3 Maltego** activity, I installed and configured Maltego on a Windows PC and visually mapped the relationship between the `networkwalks.com` domain and its associated public email address.

In the **W2-PM4 theHarvester** activity, I performed passive reconnaissance against `microsoft.com` using publicly available data sources. The exercise demonstrated how email addresses, hosts, and subdomains can be discovered without attempting to gain unauthorized access.

In the **W2-PM5 Network Scanning with Zenmap** activity, I identified my local network configuration and performed a Ping Scan against the `192.168.18.0/24` subnet. The scan discovered multiple live hosts, allowing me to collect IP and MAC address information and generate a visual network topology.

These exercises demonstrated that a significant amount of useful security information can be gathered before any exploitation takes place. Reconnaissance and network discovery help security professionals understand the visible attack surface, identify exposed information, and build a clearer picture of an environment.

I also learned the importance of documenting each step clearly, including the tools used, commands executed, results observed, potential risks, and recommended security improvements.

All activities were performed within an authorized educational scope, and no unauthorized exploitation or access was attempted.

## 8. Evidences Collected

### 8.1 W2-PM1 – Footprinting & Reconnaissance with Multiple Kali Tools

#### WHOIS Domain Information
<img width="992" height="1084" alt="whois-result" src="https://github.com/user-attachments/assets/e5e74c74-8250-4fde-b1eb-2908358a82a7" />

#### Web Technologies Fingerprinting with WhatWeb
<img width="987" height="229" alt="whatweb-result" src="https://github.com/user-attachments/assets/4115ed63-8f43-418f-bdc6-4d7201b1a1f0" />


#### DNS Resolution with Nslookup
<img width="212" height="150" alt="nslookup-result" src="https://github.com/user-attachments/assets/70a60712-ac84-4a3a-9b8e-aa68eb1151c3" />


#### HTTP Response Headers with Curl
<img width="1056" height="254" alt="curl-result" src="https://github.com/user-attachments/assets/e580c275-2817-476f-86a3-58573108a53b" />


#### Web Application Firewall Detection with Wafw00f
<img width="740" height="372" alt="wafw00f-result" src="https://github.com/user-attachments/assets/3b11e7f4-9eb1-4095-a63f-eef55bb6d46d" />


#### DNS Enumeration with DNSRecon
<img width="929" height="459" alt="dnsrescon_result" src="https://github.com/user-attachments/assets/44a9a096-4287-45dd-9452-767fe6c3e5c1" />


---
### 8.2 W2-PM2 – Footprinting with Google Hacking Database (GHDB)

#### Summary of Results (Task 1 & Task 2)
<img width="421" height="1180" alt="dORKS" src="https://github.com/user-attachments/assets/648c09be-ea8c-4f8d-9d59-f69a967c495f" />
<img width="900" height="695" alt="exposed-camera" src="https://github.com/user-attachments/assets/e61ff294-da14-4131-8403-466775ac7ea1" />
<img width="1270" height="1259" alt="ghdb-menu" src="https://github.com/user-attachments/assets/64152c29-97c4-4355-97b0-9ea71ab90468" />
[ghdb-results-table.pdf](https://github.com/user-attachments/files/31275510/ghdb-results-table.pdf)
<img width="1149" height="1036" alt="google-dork-cam" src="https://github.com/user-attachments/assets/b9d594af-3ff3-439a-a318-0c6b8c13df26" />



If you want to view the full detailed list as a downloadable document, you can click the link below:
[📥 Download the GHDB Results PDF](evidences/w2-pm2/ghdb-results-table.pdf) [ghdb-results-table.pdf](https://github.com/user-attachments/files/31275564/ghdb-results-table.pdf)


---
### 8.3 W2-PM3 – Footprinting with Maltego

#### Maltego Installation and Run as Administrator
<img width="2310" height="1254" alt="maltego-install" src="https://github.com/user-attachments/assets/4286adf7-bceb-4f80-8947-42b15d3b156f" />


#### Maltego Welcome and Activation
<img width="2307" height="1262" alt="maltego-activation" src="https://github.com/user-attachments/assets/4ab5ec0f-f8ac-4d8f-8358-10e5e76bddfb" />


#### Graph Workspace and Domain Search
<img width="2303" height="1276" alt="maltego-workspace" src="https://github.com/user-attachments/assets/3d34c19b-9eb4-4282-b42a-751196a99bdf" />



#### Setting Target Domain to networkwalks.com
<img width="2306" height="1276" alt="maltego-domain-setup" src="https://github.com/user-attachments/assets/27f67a7a-6582-4093-b246-01eb6a42b96c" />


#### Running Email Transforms
<img width="2560" height="1440" alt="maltego-email-transform" src="https://github.com/user-attachments/assets/42762b71-188f-457d-a36f-d468396169a1" />


#### Email Discovery Result
<img width="2305" height="1260" alt="maltego-email-discovery" src="https://github.com/user-attachments/assets/73102426-d4b5-4ef0-bc2a-aacdca68e4d5" />


---
### 8.4 W2-PM4 – Footprinting & Reconnaissance with theHarvester

#### theHarvester Usage and Available Options
<img width="1282" height="1399" alt="theharvester-usage" src="https://github.com/user-attachments/assets/52c26d47-d7bf-4ccd-8364-ac1f5975beae" />


#### Passive Reconnaissance Using Baidu (Emails & 22 Hosts)
<img width="708" height="1058" alt="theharvester-baidu-result" src="https://github.com/user-attachments/assets/46d01ce7-1e05-46d2-9e92-b41a09d0bef7" />


#### Passive Reconnaissance Using All Sources (API Key Missing)
<img width="554" height="1348" alt="theharvester-all-sources" src="https://github.com/user-attachments/assets/3b0e1096-c81c-4e1a-b4fb-cfb333feadec" />


---
### 8.5 W2-PM5 – Network Scanning with Zenmap

#### Zenmap Installation and Setup
<img width="903" height="737" alt="Zemap-Setup" src="https://github.com/user-attachments/assets/3a8bc082-8638-4d7f-901a-105c93a6aa0b" />
<img width="1168" height="1317" alt="Zemap install" src="https://github.com/user-attachments/assets/781da1c1-0e82-463e-8330-51f62aece894" />


#### Local IP Identification via `ip addr`
<img width="907" height="894" alt="ip-addr-result" src="https://github.com/user-attachments/assets/5bc90ea8-9e71-4ae0-bc35-f75467eabc26" />


#### Host IP and MAC Address Details in Nmap Output (Also contains Live Host List)
<img width="766" height="729" alt="zenmap-output-details" src="https://github.com/user-attachments/assets/1b32abb5-7ae4-44e1-a5be-7a525ae7f951" />


#### Network Topology (Fisheye View)
<img width="1278" height="1401" alt="zenmap-network-topology" src="https://github.com/user-attachments/assets/78b6d539-f642-4fe3-8690-ef3627419b77" />


#### Full Subnet Host List
[📥 Download the full host list (PDF)](evidences/w2-pm5/zenmap-full-host-list.pdf) 
[zenmap-full-host-list.pdf](https://github.com/user-attachments/files/31275751/zenmap-full-host-list.pdf)


---

## 9. Permission & Authorization Letter

All penetration testing activities described in this report were performed strictly under the official authorization of the Client (Networkwalks). The official Letter of Authorization for Cybersecurity Testing confirms the authorized scope, dates, and conditions of the testing engagement.

**Reference No:** NW-LOA-B082-017  
**Valid Period:** 19 August 2026 to 24 August 2026  
**Authorized Tester:** Jenik Shrestha (Intern, Batch B082)

You can download and view the full signed authorization letter below:
[📥 Download the Signed Authorization Letter (PDF)](./Permission-Letter.pdf) 
[W2-PM  Permission Letter.pdf](https://github.com/user-attachments/files/31275764/W2-PM.Permission.Letter.pdf)


---

# -End-

## 👤 Author

**Jenik Shrestha**  
Cybersecurity Trainee | B082  
Networkwalks Cybersecurity Program  
*www.linkedin.com/in/jenikshrestha*

---

## 📌 Project Information

**Program Name:** Cybersecurity Program at Networkwalks  
**Week:** 02  
**Modules Completed:** W2-PM1 | W2-PM2 | W2-PM3 | W2-PM4 | W2-PM5  
**Repository:** GitHub  
**Project Area:** Footprinting, Reconnaissance, GHDB, OSINT & Network Scanning
