# dubbo-test
一个使用Dubbo实现远程过程调用的小Demo

这里共有以下3个工程：

(1)dubbo-a工程：服务的调用者；

(2)dubbo-b工程：服务的提供者；

(3)dubbo-b-api工程：服务接口；

原理：dubbo-b工程只提供服务的实现，并通过dubbo的配置文件将服务注册到zookeeper；

      dubbo-b-api工程只是一个服务的接口，并没有任何实现；
      
      dubbo-a是服务的消费者，在其dubbo的配置文件中指定访问所在的zookeeper地址，并在其pom文件中配置好对dubbo-b-api接口的依赖；
      
      
项目启动步骤：

(1)启动zookeeper；

(2)将dubbo-b工程在web容器（比如tomcat）中启动；

(3)运行dubbo-a中的测试方法；
