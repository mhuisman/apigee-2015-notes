Security Extensions in Apigee Edge: HMAC, HttpSignature

https://github.com/apigee/iloveapis2015-hmac-httpsignature

Lots of companies using Signatures: aws, google maps, twitter, azure storage, github, et. al.

Why use signatures?
* TLS good for point to point security, but what about message relays or storage?
* message level signatures protect the payload: whole payload, selected fields.
* level of protection 

SFLY use case: Make My Book project

SHA-1, SHA-256, SHA-512

MAC: message authentication code, verifies integrity of a message. message unchanged.  message can include a subset of the entire request or the canonical representation of the entirety of the request.

HMAC: shared keyed-hash MAC, injects a key into the hashing function.  simultaneously verify both integrity and authentication of a message. message unchanged, and sender is who you expected them to be.

No opinion about keys or key structure/storage/usage.

Consumer secret - shared key used to generate HMAC (in apigee)

Can we verify HMACs in API proxies?  Not today...?

BUT WAIT (oh god) THERE'S MORE

https://github.com/apigee/iloveapis2015-hmac-httpsignature

java callout policy to create and verify HMAC signatures

not part of standard Apigee deployment, will require upload of hmac-edge-callout.jar

---

HTTPSignature

Used to sign HTTP requests in particular, and a subset of HTTP request headers in particular.

Verify signatures passed with payloads; reject request replays and altered messages.

Clients are required to generate signatures, either using public/private key or shared secret keys

**REQUIRED**: Signature algorithms are determined by server static configuration, not by client specification.  Letting client specify signature hashing algorithm is a major security hole!