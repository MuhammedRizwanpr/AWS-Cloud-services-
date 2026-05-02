**Amazon EC2 (Elastic Compute Cloud)** is a service that lets you create and use virtual servers in the cloud instead of buying physical computers. With EC2, you can launch a **Instance** means server or computer  in minutes, choose its operating system (like Linux or Windows), and install any software or application you need. You have full control over the server, just like a real machine, but AWS takes care of the physical hardware, networking, and availability. It is mainly used to host websites, run applications, perform testing, or build custom environments, and you only pay for the time you use the server.

### Advantages of EC2

- **Full control**  You can install anything (tools, OS, configs)
- **Flexible**  Choose CPU, RAM, storage as needed
- **Scalable**  Increase/decrease resources anytime
- **Pay-as-you-go**  No need to buy hardware
- **Good for learning & hacking labs**  You control everything

### Disadvantages of EC2

- **You manage everything**  OS updates, patches, security
- **Time-consuming setup**  Not instant like Lambda
- **Requires knowledge**  Networking, Linux, security
- **Risk of misconfiguration**  Can expose server if not secured properly
- **Cost can increase** if not monitored

### terminology

- **AMI** : Template it mean we can create a full package of using machine and make same like another machine 
- **Instance** : Server/computer we build 
- **Instance Type** : CPU,RAM,GPU,SSD 
- **Key Pair** : Login to the instance through SSH or RDP other protocols 
- **Security Group** : Firewall to prevent attack and control the traffic to the server 
- **EBS** : Storage/hard disk of the instance 
- **VPC** : Network