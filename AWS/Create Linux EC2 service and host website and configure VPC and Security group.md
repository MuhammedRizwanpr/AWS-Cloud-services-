Summary :
This Document and Report for show that step by step how to creating Linux instance by EC3 service and host a simply wesite on custom VPC and security group for secure the server.

## 1. Create VPC
-  You need to create VPC so go on VPC and click Create VPC and enter VPC name , CIDR, etc.. 
![[Pasted image 20260501165549.png]]


## 2. Create Internet Gateway 
Then only we can connect the subnet to the internet so go on the create Internet gateway there is already have gateway but need to create another click create 
and give name for gateway 
![[Pasted image 20260501174810.png]]

## 3. Attach the Internet Gateway to VPC 
On the top we can see attach VPC click it and enter name of VPC 
![[Pasted image 20260501175114.png]]

## 4. Create Subnets 
Here we create 2 subnet one is private and one is public. Public can access the internet in private it can communicate with only in local system so on the subnets and create here enter our VPC inside that will create the subnets so we should enter subnet CIDR based on the VPC 
![[Pasted image 20260501182703.png]]

## 5. Create Route table for public 
go to  create route table enter name and click create 
![[Pasted image 20260501183257.png]]

## 6. Set Gateway to route table 
So Edit the route table and in target select  the Internet gateway and destination 0.0.0.0/0 and add the public subnet to this route table by there is option subnet association 

So next create same way a route table no need to edit and add gateway just associate with private gateway.

## Network setup is over 
## 7. Create Linux machine EC2
Go EC2 and lunch instance and select Amazon linux and default instance type and AMI be sure it have free teir eligible

Network add the VPC we create and subnet add the public and also select the ssh , http , https because ssh for connect the instance and https and http for website access. 
![[Pasted image 20260501203551.png]]

And add create a new security group for prevent the unknow access to the ssh port for secure.

![[Pasted image 20260501203708.png]]
Now we can the instance is successfully lunched 
![[Pasted image 20260501204745.png]]
## 8. Connect the linux through SSH port 
So default user name of linux is **ec2-user** 
if we got error to connect the SSH port because the pair key file is access to every one so make it access only root then reconnect it.
![[Pasted image 20260501210047.png]]

## 9. Host the website into this linux so first download apache2 
![[Pasted image 20260501211450.png]]

## 10. upload the html file into linux and host it 
Download the apache2 in httpd and start it and upload the index.html file my system to linux server then move it own the /var/www/html 
![[Pasted image 20260501214309.png]]
![[Pasted image 20260501220022.png]]

## 11. adding Application Load Balancer 
First create one more instance on another availability zone so if any things happen in main server zone application load balancer will transfer the request to that server then make target group on load balancer 
![[Pasted image 20260502000012.png]]

### Next is make Application Load Balancer ( ALB )
go to load balancers create and select application then enter name then select internet facing means it for internet connected and that through balance the load internal mean in locally balance the load 

![[Pasted image 20260502001704.png]]

visit the page 
![[Pasted image 20260502003020.png]]
Refresh and visit again see the another server web site 
![[Screenshot from 2026-05-02 00-29-33.png]]

## Conclusion 
This website was successfully deployed using Amazon Web Services by creating and configuring an EC2 instance within a custom VPC to ensure a secure and isolated network environment. The infrastructure was designed with proper subnetting and routing, and security was enforced through the use of Security Groups to control inbound and outbound traffic. A Load Balancer was integrated to distribute incoming user requests efficiently across resources, improving availability and performance. Finally, the website was hosted on the EC2 instance, demonstrating a complete cloud deployment process that includes networking, security, scalability, and web hosting within AWS.
