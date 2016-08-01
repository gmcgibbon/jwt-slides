## Putting it all together

- Base64-encode the header, payload, and signature
- Concatenate each section of the JWT with a period `.`

```ruby
# Base64-encoded header JSON
header    = 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9'
# Base64-encoded payload JSON
payload   = 'eyJpYXQiOjE0NzAwMjk4NTUsImVtYWlsIjoidXNlckBhd2Vzb21lLmNvbSJ9'
# Base64-encoded encrypted signature
signature = 'g5oqWc74mZWaK5oJJPB6EMw8HyYc4hjnxcXQuIU5lEY='
# The full JWT
jwt       = "#{header}.#{payload}.#{signature}"
```
