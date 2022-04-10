See the overall picture of <b>implementations on microservices with .net tools</b> on real-world <b>e-commerce microservices</b> project;

<img src="https://user-images.githubusercontent.com/1147445/110304529-c5b70180-800c-11eb-832b-a2751b5bda76.png" alt="Microservices AspNetCore">

There is a couple of microservices which implemented <b>e-commerce</b> modules over <b>Catalog, Basket, Discount</b> and <b>Ordering</b> microservices with <b>NoSQL (MongoDB, Redis)</b> and <b>Relational databases (PostgreSQL, Sql Server)</b> with communicating over <b>RabbitMQ Event Driven Communication</b> and using <b>Ocelot API Gateway</b>.

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
  <li>Use <b>Portainer</b> for Container lightweight management UI which allows you to easily manage your different Docker environments</li>
  <li><b>pgAdmin PostgreSQL Tools</b> feature rich Open Source administration and development platform for PostgreSQL</li>
</ul>

## Docker Compose establishment with all microservices on docker;
<ul>
  <li>Containerization of microservices</li>
  <li>Containerization of databases</li>
  <li>Override Environment variables</li>
</ul>

## Run The Project
You will need the following tools:
<ul>
  <li><a href="https://visualstudio.microsoft.com/downloads/">Visual Studio 2019 or Later</a></li>
  <li><a href="https://dotnet.microsoft.com/en-us/download/dotnet">.Net Core 5 or later</a></li>
  <li><a href="https://www.docker.com/products/docker-desktop/">Docker Desktop</a></li>
</ul>

<h3> Installing </h3>
Follow these steps to get your development environment set up: (Before Run Start the Docker Desktop)
<ol type="1">
  <li>Clone the repository</li>
  <li>Once Docker for Windows is installed, go to the <b>Settings > Advanced option</b>, from the Docker icon in the system tray, to configure the minimum amount of memory and CPU like so:</li>
      <ul>
        <li><b>Memory: 4 GB</b></li>
        <li>CPU: 2</li>
      </ul>
  <li>At the root directory which include </b>docker-compose.yml</b> files, run below command:</li>
<pre><span class="pl-smi">docker</span><span class="pl-k">-</span><span class="pl-smi">compose</span> <span class="pl-k">-</span><span class="pl-smi">f</span> <span class="pl-smi">docker</span><span class="pl-k">-</span><span class="pl-smi">compose</span>.<span class="pl-smi">yml</span> <span class="pl-k">-</span><span class="pl-smi">f</span> <span class="pl-smi">docker</span><span class="pl-k">-</span><span class="pl-smi">compose</span>.<span class="pl-smi">override</span>.<span class="pl-smi">yml</span> <span class="pl-smi">up</span> <span class="pl-k">-</span><span class="pl-smi">d</span></pre>
  <li>Wait for docker compose all microservices. That’s it! (some microservices need extra time to work so please wait if not worked in first shut)</li>
  <li>You can <b>launch microservices</b> as below urls:</li>
    <ul>
      <li>Catalog API -> <a href="http://host.docker.internal:8000/swagger/index.html">http://host.docker.internal:8000/swagger/index.html</a></li>
      <li>Basket API -> <a href="http://host.docker.internal:8001/swagger/index.html">http://host.docker.internal:8001/swagger/index.html</a></li>
      <li>Discount API -> <a href="http://host.docker.internal:8002/swagger/index.html">http://host.docker.internal:8002/swagger/index.html</a></li>
      <li>Ordering API -> <a href="http://host.docker.internal:8004/swagger/index.html">http://host.docker.internal:8004/swagger/index.html</a></li>
      <li>Shopping.Aggregator -> <a href="http://host.docker.internal:8005/swagger/index.html">http://host.docker.internal:8005/swagger/index.html</a></li>
      <li>API Gateway -> <a href="http://host.docker.internal:8010/Catalog">http://host.docker.internal:8010/Catalog</a></li>
      <li>Rabbit Management Dashboard -> <a href="http://host.docker.internal:15672">http://host.docker.internal:15672</a> -- guest/guest</li>
      <li>Portainer -> <a href="http://host.docker.internal:9000">http://host.docker.internal:9000</a> -- admin/admin1234</li>
      <li>pgAdmin PostgreSQL -> <a href="http://host.docker.internal:5050">http://host.docker.internal:5050</a> -- a.nematpour.79@gmail.com/admin1234</li>
      <li>Elasticsearch -> <a href="http://host.docker.internal:9200">http://host.docker.internal:9200</a></li>
      <li>Kibana -> <a href="http://host.docker.internal:5601">http://host.docker.internal:5601</a></li>
      <li>Web Status -> <a href="http://host.docker.internal:8007">http://host.docker.internal:8007</a></li>
      <li>Web UI -> <a href="http://host.docker.internal:8006">http://host.docker.internal:8006</a></li>
    </ul>
  <li>Launch <a href="http://host.docker.internal:8007 ">http://host.docker.internal:8007</a> in your browser to view the Web Status. Make sure that every microservices are healthy.</li>
  <li>Launch <a href="http://host.docker.internal:8006">http://host.docker.internal:8006</a> in your browser to view the Web UI. You can use Web project in order to <b>call microservices over API Gateway</b>. When you <b>checkout the basket</b> you can follow <b>queue record on RabbitMQ dashboard</b>.</li>
</ol>

<img src="https://user-images.githubusercontent.com/1147445/81381837-08226000-9116-11ea-9489-82645b8dbfc4.png" alt="Microservices AspNetCore">

## Authors
<ul>
  <li>Amir Nematpour</li>
</ul>
