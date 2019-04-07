# `/auth/verify`
Checks if token is valid.

## POST
URL: `/auth/verify`
Payload:
- `token`: Recently generated token.
Purpose: Checks if token is valid
Responses:
- 0: Valid token.
- 1: Payload is missing or too long.
- 2: SQL error.
- 9: `dt` has never been registered or was removed.
- 10: Token invalid.
Return: None