OpenID Connect - OpenID Connect 1.0 is a simple identity layer on top of the OAuth 2.0 protocol. Launched 

Do you provide 2FA?  Do you rotate your public/private keys? (Probably not)

JSW JWE JWT all part of JOSE: "JSON Object Signing and Encryption"

JWT token different from access tokens - are not opaque, self-vaidating, stateless.

"Federated identity"

Self-generated (SFLY) JWT tokens can be used by other systems - google, paypal, etc

JWT - IETF RFC 7519 - token
JWS - IETF RFC 7515 - signature
JWE - IETF RFC 7516 - encryption

JWT

* signed, optionally encrypted set of claims: issuer, subject, audience, expiration, etc
* Receiving parties can make decisions based on claims, signing party, encrypting party

JWS

* JSON representation of Signed or HMAC'ed content

JWE

* 
