Securing the APIs:
- API needs some basic level of security to prevent direct access - without this, if any consumer knows the endpoint of an API, they can hit it directly, bypassing any controls from kong
- A simple way to fix this is by implementeing an IP allowlist on each service, and then adding only the Kong IP there
- API Management is sitting behind the firewall, so any API cosumers from outside the network need some sort of authnetication to get through to API Management (only allow legit consumers through)
- This can be done with credentials:
	- user/pass
	- secret string
	- token with strong algorithm
- API management can help secure API
- Given that attackers can also impersonate teh IP address, something like [[Mutual TLS]] can be used
- Its a bad idea to not secure API

http://kong-address:8001 is part of Kong Admin API (for kong admins)
https://kong-address:8000 is part of proxy (for kong API consumers)

Port 8443 is proxy for https traffic
