# SQL Injection Vulnerability Allowing Login Bypass

## Vulnerability
SQL Injection (SQLi)

## Objective
Bypass the login functionality and access the application without valid credentials.

## Payload

```sql
administrator'--
```

## Solution

1. Opened the login page.
2. Tested the username parameter for SQL Injection.
3. Injected the following payload:

```sql
administrator'--
```

4. The SQL comment sequence (`--`) removed the password check.
5. Logged in as the administrator user.

## Impact

An attacker can bypass authentication and gain unauthorized access to user accounts.

## Result

Lab solved successfully.
