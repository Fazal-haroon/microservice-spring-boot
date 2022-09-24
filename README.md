# microservice-spring-boot
Microservice using spring boot and spring cloud
<br>
1 First we create Order and Payment service then we book order by using order service by using RestTemplate we just call payment service.
<br>
![image](https://user-images.githubusercontent.com/36573782/191600926-e03a31d4-1f16-4fd3-8f99-bba8b13ca6dc.png)
<br>
2 Create Eureka Cloud Server
<br>
![image](https://user-images.githubusercontent.com/36573782/191833684-a5bc7bc1-489c-42ed-a629-ed617e216ade.png)
<br>
We added Eureka Client in Order and Payment services.
<br>
![image](https://user-images.githubusercontent.com/36573782/191837058-98a23a35-5e99-4672-9229-f9fa8e111b3a.png)
<br>
3 Create API gateway(spring cloud gateway)
<br>
![image](https://user-images.githubusercontent.com/36573782/191844471-141577f5-c05f-47a8-8f86-ec9b0017d8b3.png)
<br>
We added Eureka Client in API Gateway
<br>
![image](https://user-images.githubusercontent.com/36573782/191845155-91ab260e-7085-41d3-8b8b-1281dbd11870.png)
<br>
Now we are using api gateway port 8989
<br>
![image](https://user-images.githubusercontent.com/36573782/191846277-bf7852fc-0fb3-4253-9abf-66a8fb51f782.png)
<br>
![image](https://user-images.githubusercontent.com/36573782/191846431-5132ab86-182e-463e-bbd3-5788e9380b9f.png)
<br>
We used H2-in memory database
<br>
![image](https://user-images.githubusercontent.com/36573782/191846967-94c2a65c-22f1-4534-9a6b-fd0da2527bc1.png)
<br>
![image](https://user-images.githubusercontent.com/36573782/191846991-0f97dd33-c882-42c2-8d34-a664df5807e8.png)
<br>
4 Now we added netflix-hystrix in our project to check fail services
<br>
![image](https://user-images.githubusercontent.com/36573782/192097012-dea528d0-d3de-40fa-8fac-5dd215b1d4ec.png)
<br>
![image](https://user-images.githubusercontent.com/36573782/192097036-61f75258-9821-4c1d-bf8e-69a61d82fae7.png)
<br>
Hystrix-Dashboard
<br>
![image](https://user-images.githubusercontent.com/36573782/192097626-b27c69cc-469a-4ef4-ad8b-8ba9867defac.png)
<br>
![image](https://user-images.githubusercontent.com/36573782/192099520-bc547348-1a3c-461b-812c-74703d6c6e3a.png)
<br>
5 Spring Cloud Config Server with Git
<br>
I created the cloud-config-server file same repo, not need to create separte repo.
<br>
Then we added bootstrp.xml, and import spring-cloud-starter-config in Order-Service, Payment-Service, and Cloud-Gateway.
<br>
![image](https://user-images.githubusercontent.com/36573782/192106662-eee3c075-359e-4420-a933-07975d9ebbe7.png)
<br>
6 Centralized Logging with the ELK stack Elasticsearch, Logstash, and Kibana. (Microservice Centralize Logging)
<br>
ElasticSearch: ElasticSearch is a NoSQL database that is based on the Lucene search engine which will helps us to store inputs/logs. (it will help us to store data)
<br>
LogStash: LogStash is a log pipeline tool that accepts inputs/logs from various sources, & exports the data to various targets. (it will help us to process the data)
<br>
Kibana: Kibana is a visualization UI Layer, which will helps developer to monitor application logs. (it will help us to view those data)
<br>
log -> data processing (LogStash) -> storage (ElasticSearch) -> visualize (Kibana)
<br>
