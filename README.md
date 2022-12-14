# Points Calculator based on customer transaction
#The rest API to get customer rewards based on customer Id


## Problem Statement

A retailer offers a rewards program to its customers, awarding points based on each recorded purchase as follows:

For every dollar spent over $50 on the transaction, the customer receives one point.

In addition, for every dollar spent over $100, the customer receives another point.

Ex: for a $120 purchase, the customer receives

`(120 - 50) x 1 + (120 - 100) x 1 = 90 points`


Given a record of every transaction during a three-month period, calculate the reward points earned for each customer per month and total. 



- The package name is structured as com.retailer.rewards
- Exception is thrown if customer does not exists.
- H2 in-memory database to store the information.
- Please check doc file provided in the project
- Install H2 db locally and run it . change the db settings in application.properties file.
- Do run the scrip.sql on H2 in memory DB to prepare the test data.

```
 http://localhost:8080/customers/{customerId}/rewards
```



1.	Check out the project 
2.	Open the project in IntelliJ(preferred)
3.	Enable Gradle Auto-import and select Java 1.8 as SDK
4.	Once Gradle import in done open database window and select H2

<img width="448" alt="image" src="https://user-images.githubusercontent.com/120545803/207680651-2f7ef55c-d8df-4df5-bf49-8c9874c67d87.png">
 
5.	Please change configuration as mentioned in below picture

<img width="446" alt="image" src="https://user-images.githubusercontent.com/120545803/207680826-03f6dbdf-734f-4e4b-a8ae-fa369566065a.png">


6.	Username and password is sa and make sure it matches application.Properties file. (this is in memory db.)
7.	Please open h2 console in IntelliJ and run the script from /bin/main/script.sql
 
8.	Please check public schema if tables are created

<img width="447" alt="image" src="https://user-images.githubusercontent.com/120545803/207680914-294f3f7f-2dfd-46a1-bcfb-bde89049f49c.png">


9.	Once tables are created please run RewardPointsCalculatorApplication.java from java/com/retailer/rewards
10.	Open postman or any similar application and click


http://localhost:8080/customers/1001/rewards 
http://localhost:8080/customers/1002/rewards 
http://localhost:8080/customers/1003/rewards
http://localhost:8080/customers/1004/rewards


<img width="447" alt="image" src="https://user-images.githubusercontent.com/120545803/207680985-f81b594a-5050-4aa5-83aa-fb6c131b2687.png">





 




