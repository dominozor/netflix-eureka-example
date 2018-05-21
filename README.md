Starting order:
  Server->
  Service (n times)->
  Client  (n times)

<b>What is Eureka?</b>

Eureka is a REST (Representational State Transfer) based service that is primarily used in the AWS cloud for locating services 
for the purpose of load balancing and failover of middle-tier servers. We call this service, the Eureka Server. Eureka also 
comes with a Java-based client component,the Eureka Client, which makes interactions with the service much easier. 
The client also has a built-in load balancer that does basic round-robin load balancing. At Netflix, a much more sophisticated 
load balancer wraps Eureka to provide weighted load balancing based on several factors like traffic, resource usage, error conditions etc to provide superior resiliency.

<b>Eureka Server</b>

The discovery server. It contains a registry of services and a REST api that can be used to register a service, deregister a service, and discover the location of other services.

<b>Eureka Service</b>

Any application that can be found in the Eureka Server's registry and is discoverable by others. A service has a logical identifier sometimes called a VIP, sometimes called a "service id", that can refer to one or more instances of the same application.

<b>Eureka Instance</b>

Any application that registers itself with the Eureka Server to be discovered by others

<b>Eureka Client</b>

Any application that can discover services
