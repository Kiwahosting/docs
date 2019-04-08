# Status Codes
Status codes are returned with every API call. They are the output of an operation, anything but 0 is a error code which means your request was not successsful.

## List of codes
1. Missing required fields or fields are too long.
2. SQL error.
3. Email in use.
4. Verification code incorrect.
5. Verification code expired.
6. Email server rejected authentication.
7. Email failed to send.
8. Not implemented.
9. Device token does not exist.
10. Token invalid.
11. No account found using email.
12. Account has already been verified.
13. Status code does not exist.

## API: Lookup a Status Code
- Request: `GET /code/:code`
- Purpose: Returns the message corresponding to a code.
- Payload: None
- Responses:
  - 0: Message fetched.
  - 13: Status code does not exist.
- Returns:
  - `message`: Status code message, if one exists
