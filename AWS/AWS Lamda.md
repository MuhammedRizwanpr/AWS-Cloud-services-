AWS Lambda is a serverless compute service that allows you to run small pieces of code (functions) without managing any servers. You simply upload your code, and it runs automatically whenever a specific event occurs, such as an API request, file upload, or scheduled task. AWS handles the infrastructure, scaling, and maintenance, so you can focus only on writing the logic of your application.

### Why we use Lambda

- No need to manage servers
- Runs only when needed (event-based)
- Reduces cost (pay only when it runs)
- Faster development and deployment

### Features of Lambda

- **Serverless execution**  
    No need to manage OS or servers
- **Event-driven**  
    Runs automatically when triggered
- **Auto scaling**  
    Handles thousands of requests automatically
- **Pay-as-you-go pricing**  
    Charged only for execution time
- **Multiple language support**  
    Supports Python, Node.js, Java, etc.
- **Integration with AWS services**  
    Works with S3, API Gateway, DynamoDB, etc.
- **High availability**  
    Runs across multiple Availability Zones
- **Short execution time**  
    Designed for quick tasks (not long-running apps)

### Disadvantages of Lambda

- **Cold start delay**  
    If the function is idle, the first request can be slow.
- **Execution time limit**  
    Max runtime is limited (not suitable for long-running tasks).
- **Hard debugging & monitoring**  
    No direct server access → troubleshooting is more complex.
- **Limited control**  
    You can’t control OS or underlying infrastructure.
- **Stateless nature**  
    No memory between executions → need external storage (S3, DB).
- **Dependency/package limits**  
    Large applications can be difficult to manage in Lambda.
- **Not ideal for all workloads**  
    Continuous or heavy applications are better on EC2/ECS.

## Create a lambda function and run 

![[Pasted image 20260502031018.png]]

Here when i call a REST API then the lambda function work so it give the data like users name and id .  create function to return the usernames 
![[Pasted image 20260502031431.png]]

Function is worked 
![[Pasted image 20260502032922.png]]
