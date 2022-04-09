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

