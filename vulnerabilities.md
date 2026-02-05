## SQL Injection (Authentication Bypass)

**Category:** OWASP A05:2025 Injection

**Description:**  
The login form failed to properly sanitize user input, allowing SQL injection.

**Steps to Reproduce:**
1. Navigate to the login page under Account
2. Enter `' OR 1=1--` as the email
3. Enter any password, I used `anything`
4. Click login

**Impact:**  
An attacker can bypass authentication and access user accounts.

**Mitigation:**  
Use parameterized queries and input validation.
