**Amazon Athena is a serverless query service that allows you to run SQL queries directly on data stored in S3 without setting up or managing any servers.** It works by reading the data from S3 when you run a query, processing it, and returning the results. This makes it useful for analyzing logs, large datasets, and application data quickly and cost-effectively, since you only pay for the amount of data scanned.

### Step-by-step working

![alt text](screenshot/Pasted%20image%2020260502040620.png)


1. **Store data in S3**
    - Put files (CSV, JSON, Parquet, logs) in Amazon S3
2. **Define schema (table structure)**
    - Tell Athena how data looks (columns, format)
    - Using Glue Data Catalog or manual table creation
3. **Write SQL query**
    - Example: `SELECT * FROM logs WHERE status = 200;`
4. **Athena reads data from S3**
    - It scans only required data (based on query)
5. **Processes the query**
    - Filters, sorts, aggregates data
6. **Stores result in S3**
    - Query output is saved in an S3 bucket
7. **Returns result to user**
    - You see output in console or download it

## Practical on Athena 
### Create two bucket for data to query and store the result 
![alt text](screenshot/Pasted%20image%2020260502040211.png)

### Query editor add the result location 
### next give data source 

### data are add into the editor now we can query 
first i see the all cars 
![alt text](screenshot/Pasted%20image%2020260502042913.png)

## Conclusion 

Using **SQL queries in Amazon Athena**, we can easily read, filter, and analyze data stored in Amazon S3 without moving it or creating a database. By using commands like `SELECT`, `WHERE`, `JOIN`, and `GROUP BY`, we can extract meaningful information such as customer details, car information, and relationships between datasets. This approach is fast, cost-effective, and useful for analyzing large amounts of data, especially logs and structured files.
