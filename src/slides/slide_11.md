## `jwt` Gem

```ruby
require 'jwt'

payload     = { key: 'value' }
secret      = '$up3r sekret Key.'
algorithm   = 'HS256'

encoded_jwt = JWT.encode(
  payload, secret, algorithm
)
# eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.
# eyJrZXkiOiJ2YWx1ZSJ9.
# o7svO0Svpe-CkK8jjh2T-Uk-YSkHyzSiJw6uACv46OE
decoded_jwt = JWT.decode(
  encoded_jwt, secret, true, algorithm: algorithm
)
# [{"key"=>"value"}, {"typ"=>"JWT", "alg"=>"HS256"}]
```
