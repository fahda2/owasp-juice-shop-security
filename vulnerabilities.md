## SQL Injection (Authentication Bypass)

**Category:** OWASP A05:2025 Injection

**Description:**  
The login endpoint fails to validate user input, allowing SQL injection to bypass authentication.

**Steps to Reproduce:**
1. Navigate to the login page under Account
2. Enter `' OR 1=1--` as the email
3. Enter any password, I used `anything`
4. Click login

**Evidence:**
- Intercepted POST request to `/rest/user/login`
- Application granted access without valid credentials

**Impact:**  
An attacker can gain unauthorized access to user accounts.

**Mitigation:**  
Use parameterized queries and proper input validation.