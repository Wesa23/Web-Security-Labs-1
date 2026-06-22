<img width="1920" height="1080" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/acd8063a-bb6e-4938-a49e-1a580e61a239" />

# SQL Injection Attack, Querying the Database Type and Version on MySQL and Microsoft SQL Server

## Vulnerability
SQL Injection (SQLi)

## Objective
Determine the database type and retrieve version information from the backend database.

## Payload

```sql
' UNION SELECT @@version, NULL#
```

أو

```sql
' UNION SELECT @@version, NULL--
```

## Solution

1. Identified a SQL Injection vulnerability in the application.
2. Determined the number of columns returned by the query.
3. Identified a column that could display string data.
4. Used the following payload:

```sql
' UNION SELECT @@version, NULL#
```

5. Retrieved the database version information from the server.

## Impact

An attacker can discover the database type and version, which helps identify known vulnerabilities and plan further attacks.

## Result

Successfully retrieved the database version and confirmed the backend database technology.
