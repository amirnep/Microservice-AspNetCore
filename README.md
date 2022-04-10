# Whats Including In This Repository
We have implemented below <b> features over the Microservice-AspNetCore repository. </b>

## Catalog microservice which includes;
<ul>
  <li>ASP.NET Core Web API application</li>
  <li>REST API principles, CRUD operations</li>
  <li><b>MongoDB database</b> connection and containerization</li>
  <li>Repository Pattern Implementation</li>
  <li>Swagger Open API implementation</li>
</ul>

## Basket microservice which includes;
<ul>
  <li>ASP.NET Web API application</li>
  <li>REST API principles, CRUD operations</li>
  <li><b>Redis database</b> connection and containerization</li>
  <li>Consume Discount <b>Grpc Service</b> for inter-service sync communication to calculate product final price</li>
  <li>Publish BasketCheckout Queue with using <b>MassTransit and RabbitMQ</b></li>
</ul>

## Discount microservice which includes;
<ul>
  <li>ASP.NET <b>Grpc Server</b> application</li>
  <li>Build a Highly Performant <b>inter-service gRPC Communication</b> with Basket Microservice</li>
  <li>Exposing Grpc Services with creating <b>Protobuf messages</b></li>
  <li>Using <b>Dapper for micro-orm implementation</b> to simplify data access and ensure high performance</li>
  <li><b>PostgreSQL database</b> connection and containerization</li>
</ul>

## Microservices Communication
<ul>
  <li>Sync inter-service <b>gRPC Communication</b></li>
  <li>Async Microservices Communication with <b>RabbitMQ Message-Broker Service</b></li>
  <li>Using <b>RabbitMQ Publish/Subscribe Topic</b> Exchange Model</li>
  <li>Using <b>MassTransit</b> for abstraction over RabbitMQ Message-Broker system</li>
  <li>Publishing BasketCheckout event queue from Basket microservices and Subscribing this event from Ordering microservices</li>
  <li>Create <b>RabbitMQ EventBus.Messages library</b> and add references Microservices</li>
</ul>

## Ordering Microservice
<ul>
  <li>Implementing <b>DDD, CQRS, and Clean Architecture</b> with using Best Practices</li>
  <li>Developing <b>CQRS with using MediatR, FluentValidation and AutoMapper packages</b></li>
  <li>Consuming <b>RabbitMQ</b> BasketCheckout event queue with using <b>MassTransit-RabbitMQ</b> Configuration</li>
  <li><b>SqlServer database</b> connection and containerization</li>
  <li>Using <b>Entity Framework Core ORM</b> and auto migrate to SqlServer when application startup</li>
</ul>

## API Gateway Ocelot Microservice
<ul>
  <li>Implement <b>API Gateways with Ocelot</b></li>
  <li>Sample microservices/containers to reroute through the API Gateways</li>
  <li>Run multiple different <b>API Gateway/BFF</b> container types</li>
  <li>The Gateway aggregation pattern in Shopping.Aggregator</li>
</ul>

## WebUI ShoppingApp Microservice
<ul>
  <li>ASP.NET Core Web Application with Bootstrap 4 and Razor template</li>
  <li>Call <b>Ocelot APIs with HttpClientFactory and Polly</b></li>
</ul>

## Microservices Cross-Cutting Implementations
<ul>
  <li>Implementing <b>Centralized Distributed Logging with Elastic Stack (ELK); Elasticsearch, Logstash, Kibana and SeriLog</b> for Microservices</li>
  <li>Use the <b>HealthChecks</b> feature in back-end ASP.NET microservices</li>
  <li>Using <b>Watchdog</b> in separate service that can watch health and load across services, and report health about the microservices by querying with the HealthChecks</li>
</ul>

## Microservices Resilience Implementations
<ul>
  <li>Making Microservices more <b>resilient Use IHttpClientFactory</b> to implement resilient HTTP requests</li>
  <li>Implement <b>Retry and Circuit Breaker patterns</b> with exponential backoff with IHttpClientFactory and <b>Polly policies</b></li>
</ul>

## Ancillary Containers
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
