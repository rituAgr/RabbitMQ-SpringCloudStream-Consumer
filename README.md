##Spring Cloud Stream Application - Message-Consumer

###Inorder to locally do the following - 

1. Run ```docker run -d --hostname local-rabbit --name demo-rmq -p 15672:15672 -p 5672:5672 rabbitmq:3.6.11-management```
2. Then start the application.
3. if there is any message. It will automatically consume it.


###Inorder to run the application over pcf
1. Create rabbit-test instance at pcf, if not present.
2. ```gradle clean build```
3. ```cf push``` This will take the manifest file at home directory of application and deploy application at PCF.
4. If incase we want to see actually message be consumed. Insert log. Currently, its not there.

###Note:

1. All properties for pcf are binded by vcap.service, but the port because it was unable to convert String to Int over pcf.
2. For looking at producer side look for RabbitMQ-SpringCloudStream-Producer repo.

 
