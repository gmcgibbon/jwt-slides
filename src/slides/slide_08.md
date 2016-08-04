## Signature

- An encrypted summary of the header and payload sections
- Can be used to validate integrity of a received JWT

```ruby
require 'base64'
require 'openssl'
require 'json'

def encode(str); Base64.urlsafe_encode64(str); end

header  = { typ: 'JWT', alg: 'HS256' }
payload = { iat: 1470029855, email: 'user@awesome.com' }

encoded = "#{encode(header.to_json)}.#{encode(payload.to_json)}"

key       = 'sekret'
digest    = OpenSSL::Digest::SHA256.new()
signature = encode(OpenSSL::HMAC.digest(digest, key, encoded))
```
