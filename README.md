# Mortulus dev-auth issuer

Public signing keys and the OpenID discovery document for the Mortulus developer login.
This repository contains no secrets. Private keys live only on developer machines.

- `.well-known/openid-configuration` — discovery document (issuer and key location)
- `jwks.json` — the public keys, one per developer, by `kid`

Removing a key from `jwks.json` revokes every token that key ever signed, once the
server refetches the file.
