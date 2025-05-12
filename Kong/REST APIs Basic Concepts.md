Google provides a "Sign in using Google" login option
This can be used by other applications over the internet
Google is considered to be the API Provider
Applications that use it are called API Consumers

Why is API important?
- helps to promote their own business
	- Users gain more functionality with less effort
	- Both user and API provider gain pupoularity
- gain revenue
- protecting the source code
- a system can expose an API to get relevant data instead of exposing entire database
- consumers dont need to know the source code of the provider to access their data

REST API Basics
- its a type of web architecture
- implementation of client and server is independent of each other as long as the response is the same
- server does not need to know the state of the client (it is stateless)
	- e.g. server doesnt need to know the last thing it sent to the client, or if the lcient is logged in
- as long as the client is using the right format, the server will give a response
- currently use HTTP & JSON
- Older systems can use XML

REST API:
- It is not a technology or standard
- It is an architectural style and guideline
- not limited to any partuclar language

Principles:
- Uniform Interface: must have a unique URI (unique resource identifier)
- Client-Server - they must be independent of each other
- Stateless: no session or history saved - if this is necessary, then the client request should contain all the info to service the request, including authentication and authorization details
- Cacheable: cliuent, server, and anything else can all cache resources to improive performance
- Layered System: Service A might connect to servier B and C before getting to D, but client cannot tell, and doesn't need to know
- COde on demand (optional): e.g. client might call API to get ui widget-rendering code

PROTOCOL://DOMAIN/RESOURCE_PATH?PATHVARIABLE=2

HTTP methods:
GET - only used to read, not update/modify resource (should be indemptoent - making multiple identical requests will return the same result)
POST - create resource - calling more than once will return smilar response, with differeng ID if there is one
PUT - used to updated, calling same request should return same result (should be indemptoent)
DELETE - used to delete resource

HTTP codes:
1xx: informational
2xx: Success
3xx: Redirection
4xx: Client error
5xx: Server error
