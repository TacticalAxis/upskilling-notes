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