# `/auth/device`
Manages device tokens.

## GET
- Request: `GET /auth/device`
- Purpose: Generate a new `dt`.
- Payload: None
- Responses:
  - 0: `dt` successfully generated.
  - 2: SQL error.
- Returns:
  - `device`: The new `dt`.

## POST
- Request: `POST /auth/device`
- Payload:
  - `device`: Device token.
- Purpose: Check if `dt` is valid.
- Responses:
  - 0: `dt` is valid.
  - 1: `dt` is missing or too long for UUIDv4.
  - 2: SQL error.
  - 9: `dt` has never been registered or was removed.
- Returns: None
