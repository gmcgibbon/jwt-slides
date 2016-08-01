## Payload

- Contains a set of claims
- There are three different kinds of claims:
  - Public Claims: user-defined data
  - Private Claims: convention-based data
  - Registered Claims: metadata with reserved names

```javascript
{
  "iat":   1470029855,            // Issued at  (Registered)
  "exp":   1470116255,            // Expires at (Registered)
  "id":    25114,                 // User ID    (Public/Registered)
  "email": "user@awesome.com"     // User email (Public/Registered)
  "state": "active",              // User state (Public/Registered)

}
```
