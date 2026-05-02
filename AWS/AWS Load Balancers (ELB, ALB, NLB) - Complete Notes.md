
---

## 📌 1. What is Load Balancer

A Load Balancer distributes incoming traffic across multiple servers.

### 🎯 Goals:
- High availability
- Fault tolerance
- Better performance

---

## 📌 2. What is ELB

Elastic Load Balancing (ELB) is AWS service for load balancing.

👉 It includes:
- Application Load Balancer (ALB)
- Network Load Balancer (NLB)
- Classic Load Balancer (CLB - legacy)

---

## 📌 3. Application Load Balancer (ALB)

### 🔹 Layer:
- Layer 7 (Application Layer)

### 🔹 Protocol:
- HTTP / HTTPS

### 🔹 Features:
- Path-based routing (/api, /admin)
- Host-based routing (domain-based)
- Works with microservices
- Integrates with WAF

### 🔹 Use Cases:
- Web applications
- REST APIs
- Microservices architecture

---

## 📌 4. Network Load Balancer (NLB)

### 🔹 Layer:
- Layer 4 (Transport Layer)

### 🔹 Protocol:
- TCP / UDP

### 🔹 Features:
- Very high performance
- Low latency
- Static IP support
- Handles millions of requests

### 🔹 Use Cases:
- Gaming apps
- Real-time systems
- High-performance applications

---

## 📌 5. Classic Load Balancer (CLB)

### 🔹 Layer:
- Layer 4 & Layer 7 (limited)

### 🔹 Features:
- Old generation
- Basic load balancing
- Less flexible

### 🔹 Use Cases:
- Legacy applications

---

## 📌 6. How Load Balancer Works

1. User sends request
2. Load balancer receives it
3. Checks healthy servers
4. Forwards request to one server
5. Server responds

---

## 📌 7. Health Checks

Load balancer checks server health:

### ALB:
- HTTP request (/health)
- Expected: 200 OK

### NLB:
- TCP connection check

If failed:
- Server marked Unhealthy
- Traffic stopped

---

## 📌 8. ALB vs NLB vs CLB

| Feature | ALB | NLB | CLB |
|--------|-----|-----|-----|
| Layer | L7 | L4 | L4/L7 |
| Protocol | HTTP/HTTPS | TCP/UDP | HTTP/TCP |
| Performance | Medium | High | Low |
| Routing | Advanced | Basic | Limited |
| Use Case | Web apps | High performance | Legacy |

---

## 📌 9. Architecture Example

User → Route 53 → Load Balancer → EC2 / ECS → Response

---

## 📌 10. Final Summary

- ELB = Load balancing service
- ALB = Smart routing (Layer 7)
- NLB = Fast routing (Layer 4)
- CLB = Old version

---

## 🎯 One-Line Revision

- ALB → Smart (Application level)
- NLB → Fast (Network level)
- ELB → AWS load balancing service