# `/auth/email`
Manages email usage (if a email is taken or not), and verifying an email.

## GET
- Request: `GET /auth/email/<email>`
- Purpose: Check if email is in use by an account.
- Payload: None
- Responses:
  - 0: Email is not in use.
  - 1: Payload is missing or too long.
  - 2: SQL error.
  - 3: Email in use.
- Returns: None

## POST
- Request: `POST /auth/email`
- Purpose: Verify a user's email address. Used by `panel/verify/:code`
- Payload:
  - `code`: Email verification code, sent to the user's email.
- Responses:
  - 0: Email verified, account activated.
  - 1: Payload is missing or too long.
  - 2: SQL error.
  - 4: Invalid verification code.
  - 5: Verification code expired.
- Returns: None

## API: PUT
- Request: `PUT /auth/email`
- Payload:
  - `email`: User's email
- Purpose: Verify a user's email address.
- Responses:
  - 0: Email verified, account activated.
  - 1: Payload is missing or too long.
  - 2: SQL error.
  - 6: Email server rejected authentication.
  - 7: Email failed to send.
  - 12: Account has already been verified.
- Returns: None
