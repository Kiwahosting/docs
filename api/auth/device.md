# `/auth/device`
Manages device tokens.

## GET
URL: `/auth/device`
Payload: None
Purpose: Generate a new `dt`.
Responses:
- 0: `dt` successfully generated.
- 2: SQL error.
Return:
- `device`: The new `dt`.

## POST
URL: `/auth/device`
Payload:
- `device`: Device token.
Purpose: Check if `dt` is valid.
Responses:
- 0: `dt` is valid.
- 1: `dt` is missing or too long for UUIDv4.
- 2: SQL error.
- 9: `dt` has never been registered or was removed.
Return: None