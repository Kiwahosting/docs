# `/auth/email`
Manages email verification and usage.

## GET
URL: `/auth/email/<email>`
Payload: None
Purpose: Check if email is in use by an account.
Responses:
- 0: Email is not in use.
- 1: Payload is missing or too long.
- 2: SQL error.
- 3: Email in use.
Return: None

## POST
URL: `/auth/email`
Payload:
- `code`: Email verification code.
Purpose: Verify a user's email address.
Responses:
- 0: Email verified, account activated.
- 1: Payload is missing or too long.
- 2: SQL error.
- 4: Invalid verification code.
- 5: Verification code expired.
Return: None

## PUT
URL: `/auth/email`
Payload:
- `email`: User's email
Purpose: Verify a user's email address.
Responses:
- 0: Email verified, account activated.
- 1: Payload is missing or too long.
- 2: SQL error.
- 6: Email server rejected authentication.
- 7: Email failed to send.
- 12: Account has \already been verified.
Return: None