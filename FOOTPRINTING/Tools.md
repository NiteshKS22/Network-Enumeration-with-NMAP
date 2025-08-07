## Tools In This module

### 1. [crt.sh](https://crt.sh/)
`crt.sh` is a public certificate transparency log search engine. It allows users to search for SSL/TLS certificates issued for domains. This is useful in reconnaissance to discover subdomains or identify organizational infrastructure by finding all certificates related to a specific domain.

**Use Cases:**
- Discovering subdomains associated with a domain
- Identifying certificate misconfigurations or misissuance
- Monitoring issued certificates for a specific organization

---

### 2. [Shodan](https://www.shodan.io/)
Shodan is a search engine for internet-connected devices. It allows users to discover information about systems connected to the internet, such as servers, IoT devices, webcams, routers, etc., including details like open ports, services running, and software versions.

**Use Cases:**
- Identifying exposed services and devices
- Performing passive reconnaissance on targets
- Finding systems with known vulnerabilities

---

### 3. `dig` (Domain Information Groper)
`dig` is a command-line tool used for querying DNS name servers. It can be used to gather DNS records for a domain, such as A, MX, NS, TXT, CNAME, and more.

**Use Cases:**
- DNS enumeration and troubleshooting
- Finding IP addresses associated with domains
- Verifying DNS records like SPF, DKIM, and DMARC

**Example:**
```bash
dig example.com
dig MX example.com
dig +short TXT example.com
```

---

### 4. `curl`
curl is a command-line tool used to transfer data to or from a server using protocols like HTTP, HTTPS, FTP, and more. It’s widely used in testing APIs, web applications, and performing initial reconnaissance.

**Use Cases:**
- Making HTTP requests to a web server
- Fetching HTTP headers or response bodies
- Testing endpoints and APIs

**Example:**

```bash
curl -I https://example.com     # Fetch HTTP headers
curl -X GET https://api.example.com/data
```

### 5. [Let’s Encrypt](https://letsencrypt.org/)
`Let’s Encrypt` is a free, automated, and open certificate authority (CA) that provides SSL/TLS certificates. It's used to enable HTTPS on websites easily and securely, without the need to purchase traditional certificates.

**Use Cases:**
- Securing web applications with HTTPS
- Automating SSL certificate issuance and renewal
- Demonstrating trust via certificate transparency logs

**Tools Integration:**
- Works with tools like Certbot for easy setup
- Visible in crt.sh logs, making it useful for reconnaissance

**Example (using Certbot):**

```bash
sudo certbot --nginx -d example.com
```
