# `/auth/signup`
Creates new accounts.

## POST
Request: `POST /auth/signup`
- Payload:
  - `password`: Password hashed using SHA256
  - `email`: User's email
  - `firstName`: User's first name
  - `lastName`: User's last name
- Purpose: Create a new account for this user.
- Responses:
  - 0: Account created.
  - 1: Payload is missing or too long.
  - 2: SQL error.
  - 3: Email in use.
- Returns: None
