# Community
## Introduction
A discussion community project. It not only includes registration, login, posting, commenting, liking, and replying functions, but also realizes sensitive word filtering using prefix tree, generates growth charts and pdfs using wkhtmltopdf, realizes website UV and DAU statistics, and stores user avatars and other information on the cloud server.
 <img width="960" alt="framework" src="https://user-images.githubusercontent.com/67742649/206989138-e44b3cf8-6349-4228-959a-2f986eed5dd0.png">
 ![image](https://user-images.githubusercontent.com/67742649/211079116-4c56c564-228a-4fb9-8d63-9089e2cd07ec.png)
 
 
 ![image](https://user-images.githubusercontent.com/67742649/211079263-a4ec451e-0fae-4726-9a16-97c455002b2d.png)

 ## Functions
 - Used **Spring Security** to implement permission control, instead of the interceptor, and used their own authentication scheme instead of the Security authentication process, which made permission authentication and control more convenient and flexible.
 - Used **Redis** set for likes, zset for follows, and used Redis for storing login tickets and authentication codes to solve the distributed session problem.
 - Used Redis advanced data type **HyperLogLog** to count UV  (Unique Visitor) and **Bitmap** to count DAU (Daily Active User).
 - Built a  powerful asynchronous messaging system using **Kafka** to handle sending system notifications such as comments, likes and follows, and encapsulating them using events.
 - Used **Elasticsearch** to implement the global search and add features such as keyword highlighting.
 - Used distributed cache **Redis** and local cache **Caffeine** as multi-level cache to avoid cache avalanche for the hot post ranking module, which increases QPS by 20 times; used **Quartz** to update the hot post ranking regularly.
 ## Display
 - Index
![1](https://user-images.githubusercontent.com/67742649/206989205-74d534d9-4df7-47b5-adbc-b5dde3213e74.png)
 - Message
![2](https://user-images.githubusercontent.com/67742649/206989240-ec01b35c-cfca-4a52-8c7d-6f8e967aa9b4.png)



