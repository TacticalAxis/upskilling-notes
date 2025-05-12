REST APi Types:
From API Management perspective, we can group API by consumer
Private/Internal: consudmer of API and creator of API are from the same organisation
Partner: Can be used by different organsiation based on agreement, usage based on said agreement
Public: open for everythiin, anyone can request access and use, credentials per user

API Management:
- creating and publishing API
- Enforcing usage policies
- Controlling access and traffic
- Collect & analyse usage statistics
- Performance reporting
- API Gateway (single access point for consumer)

Writing code for API management in the API itself isn't smart because the API should focus on the business logic itself
APIs have request per minute or DDoS protection, or API keys, and writing all this inside each API is not a good idea because if anything changes, there would also be a lot of code changes

Behaviour should be consistent among services
All the written code for API management should contain the same logic
We should use API management functionality to add things like API key or request limiting

Examples of API management tools:
- Kong
- axway
- apigee
- MuleSoft
- 3scale (by red hat)
- tyk.io
- IBM Api Connect
- Mashery
- WSO2 API Manager

Kong:
- Based on Nginx
- PostgreSQL or Cassandra
- Free & Enterprise Edition
- User Interface
- Easy Installation
- Scalable & Configurable
- Plugins - Free & Enterprise


API Management
- Hit rate limit
- Traffic control logic
- Max request size
- Authentication/Authorisation
- API Keys

Can modify all traffic control logic without affecting API business logic
Acts as an API gateway, takes client request, route the right service, passes the response
THere there are IP changes etc, config only changes in API management, not all the services

Ports:
5432 : PostgreSQL. If you have a runningPostgreSQL server, please stop it since we will use Docker PostgreSQL.
8000 : Kong gateway (via plain HTTP)
8443 : Kong gateway (via HTTPS)
8001 : Kong admin API
8002 : Kong Manager UI
9001, 9002, 9003, 9004 : Dummy services (alpha, beta, gamma, omega)

Optional ports"
9411 : Zipkin. We will use it on lecture about distributed tracing
9200, 9600, 5555, 5601 : Elastic stack (Elasticsearch, Logstash, Kibana). We will use it on lecture about API analytics
80, 443 : Kong gateway (optional, on one lesson we will change ports)