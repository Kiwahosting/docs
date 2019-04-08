# `/auth/signin`
Manages account logins.

## POST
- Request: `POST /auth/signin`
- Purpose: Connect `dt` to account.
- Payload:
  - `email`: Email used to login.
  - `token`: Recently generated token.
- Responses:
  - 0: Successful signin.
  - 1: Payload is missing or too long.
  - 2: SQL error.
  - 9: `dt` has never been registered or was removed.
  - 10: Token invalid.
  - 11: No account found using email.
- Returns: None
