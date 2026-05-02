Why IAM ( Identity and Access Management ) need because "It's not Me and My cloud, It's We and Our cloud" this means the cloud is not using by a single employee, in a company there will be so many users so without proper knowledge there will be more mistake and more damage it cause for loss money and brake service of company so each user give their permission for only to do there daily work.

IAM Identity and Access management here identity mean for authentication and access management for authorization,

This provide the infrastructure to control who , can access , what 

The Principle of least privilege - its very important 
- Only give minimum level of privilege necessary to perform the duties 
##### **IAM Users** : It means users they have some permission to do operation 
##### **IAM Policy** : The rule or permission that give to the users.

##### **IAM Group** : here we can make a group of users they have same policy.

##### **IAM Role** : This is temporary IAM user. we can create policy but it not in long term it in short term a specific time after this user will remove. It's mainly for new worker come do work so giving the temporary privilege for secure.

IAM policies write in Json format 

There is different type of policy it is Identity based policies and resource based policy
Identity based policy is use to assign the which user to the service and Resource based policy is permission assign to the resources 

### Advantages

- **Fine-grained access control**  
    You can give exact permissions (read, write, admin) to specific users or services.
- **Improved security**  
    Instead of sharing passwords, you create **separate users and roles** → safer system.
- **Centralized management**  
    Manage all users, permissions, and access policies from one place.
- **Supports MFA (Multi-Factor Authentication)**  
    Adds extra security layer beyond password.
- **Temporary access with roles**  
    You can give short-term access (useful for apps, EC2, Lambda).
- **No extra cost**  
    IAM itself is free in AWS.

### Disadvantages

- **Complex to understand (at first)**  
    Policies, roles, permissions can confuse beginners.
- **Misconfiguration risk**  
    Wrong permission (like `*:*`) can expose full AWS account.
- **Debugging access issues is hard**  
    If something doesn’t work, finding which policy is blocking can be tricky.
- **Too many permissions = security risk**  
    If not managed properly, users may get more access than needed.
- **Learning curve**  
    Requires understanding of JSON policies and AWS services.

## Create a IAM user and Policies 

user is created biluIAM ![[Pasted image 20260502013808.png]]

Here this user unable to list buckets 

![[Pasted image 20260502014939.png]]

## Create policy to see the list bucket.

![[Pasted image 20260502015837.png]]

## Add that policy to the user 
![[Pasted image 20260502020007.png]]

## Now the user can see the list of buckets 
![[Pasted image 20260502020131.png]]
