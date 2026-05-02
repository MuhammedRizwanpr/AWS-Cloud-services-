
---

## 📌 1. What is DNS

DNS (Domain Name System) converts:
- Domain name → IP address

Example:
google.com → 142.250.x.x

---

## 📌 2. What is Amazon Route 53

Amazon Route 53 is AWS DNS service.

👉 It acts as:
- Domain registrar
- DNS manager
- Traffic router

---

## 📌 3. How Route 53 Works

1. User enters domain (example.com)
2. Request goes to DNS resolver
3. Resolver queries:
   - Root server
   - TLD (.com)
   - Authoritative DNS (Route 53)
4. Route 53 returns IP or endpoint
5. Browser connects to server

---

## 📌 4. Key Components

### 🔹 Hosted Zone
- Container for DNS records

### 🔹 Record Types
- A → domain to IP
- CNAME → domain to domain
- MX → mail servers
- NS → name servers

---

## 📌 5. Routing Policies

- Simple routing
- Weighted routing
- Latency-based routing
- Failover routing

---

## 📌 6. Use Cases of Route 53

- Connect domain to EC2 / ECS / Load Balancer
- Global traffic management
- High availability setup

---

## 📌 7. Important Points

- Route 53 is Authoritative DNS
- It does NOT store website content
- It only maps domain → resource

---

# 🛡️ AWS WAF (Web Application Firewall)

---

## 📌 8. What is AWS WAF

AWS WAF protects web applications from attacks.

👉 It filters HTTP/HTTPS requests

---

## 📌 9. What it Protects Against

- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)
- Bots and bad traffic
- Rate-based attacks

---

## 📌 10. How WAF Works

1. User sends request
2. Request hits WAF
3. WAF checks rules
4. Allow or Block

---

## 📌 11. Where WAF is Used

- CloudFront
- Application Load Balancer (ALB)
- API Gateway

---

## 📌 12. Rule Types

- IP block/allow
- Geo blocking
- Rate limiting
- Managed rule sets (AWS rules)

---

## 📌 13. WAF vs Security Group

| Feature | WAF | Security Group |
|--------|-----|---------------|
| Layer | L7 (Application) | L4 (Network) |
| Checks | HTTP content | IP & Port |
| Use | Attack filtering | Access control |

---

## 📌 14. Real Architecture

User → Route 53 → Load Balancer → WAF → EC2/ECS

---

## 📌 15. Final Summary

- Route 53 = DNS (domain → IP)
- WAF = Web security filter
- Route 53 routes traffic
- WAF protects traffic

---

## 🎯 One-Line Revision

- Route 53 → "Where to go"
- WAF → "Is it safe to allow"