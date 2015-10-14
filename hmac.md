Security Extensions in Apigee Edge: HMAC, HttpSignature

https://github.com/apigee/iloveapis2015-hmac-httpsignature

Lots of companies using Signatures: aws, google maps, twitter, azure storage, github, et. al.

Why use signatures?
* TLS good for point to point security, but what about message relays or storage?
* message level signatures protect the payload: whole payload, selected fields.
* level of protection 

SHA-1, SHA-256, SHA-512

MAC: message authentication code, verifies integrity of a message. message unchanged.

HMAC: shared keyed-hash MAC, injects a key into the hashing function.  simultaneously verify both integrity and authentication of a message. message unchanged, and sender is who you expected them to be.

No opinion about keys or key structure/storage/usage.

Consumer secret - shared key used to generate HMAC (in apigee)

Can we verify HMACs in API proxies?  Not today...?

BUT WAIT (oh god) THERE'S MORE

