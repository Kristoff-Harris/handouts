# List of generic checks (non-specific)

## Authorization

- [ ] Identify Roles
- [ ] Identify sensitive/privileged endpoints
- [ ] Identify authz expectations specific to the business purpose of the app
  * Can non-privileged users view, add, or alter accounts?
  * Is there functionality to add accounts with higher access levels than their own access?
  * How is separation of duties handled?
- [ ] Identify Authorization functions/filtes
  * Do they take Tokens? Cookies? Custom or handled by a framework?

* Broken Access Control
  - [ ] Insecure Direct Object Reference (`find_by`, `find`, `findOne`, `findAll`, etc)
  - [ ] Missing Function Level Access Control
  - [ ] Verify Authorization Filters
  
* Generic authz flaws
  - [ ] Sensitive Data Exposure
  - [ ] Mass Assignment
  - [ ] Business Logic Flaws
  - [ ] Are CSRF Protections applied correctly
  - [ ] Are users forced to re-assert their credentials for requests that have critical side-effect (account changes, password reset, etc)?

## Authentication

* Authentication function checks

- [ ] Password hashing mechanism
- [ ] Timing attacks - this could be username/password or HMAC operations verifying keys
- [ ] Forgot Password
- [ ] 2 factor auth
- [ ] Enumeration... if it matters
- [ ] Signup
- [ ] Brute force attacks
- [ ] Session Management Issues
  - [ ] Session Fixation
  - [ ] Session Destruction
  - [ ] Session Length

## Auditing

- [ ] If an exception occurs, does the application fails securely?
- [ ] Do error messages reveal sensitive application or unnecessary execution details?
- [ ] Are Component, framework, and system errors displayed to end user?
- [ ] Does exception handling that occurs during security sensitive processes release resources safely and roll back any transactions?
- [ ] Are relevant user details and system actions logged?
- [ ] Is sensitive user input flagged, identified, protected, and not written to the logs?
  * Credit Card #s, Social Security Numbers, Passwords, PII, keys


## Datastore

## File handling
