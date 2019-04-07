# `/auth/signin`
Manages account logins.

## POST
URL: `/auth/signin`
Payload:
- `email`: Email used to login.
- `token`: Recently generated token.
Purpose: Connect `dt` to account.
Responses:
- 0: Successful signin.
- 1: Payload is missing or too long.
- 2: SQL error.
- 9: `dt` has never been registered or was removed.
- 10: Token invalid.
- 11: No account found using email.
Return: None