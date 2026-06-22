<img width="1920" height="1080" alt="Screenshot (1)" src="https://github.com/user-attachments/assets/4055ead7-3ead-4818-bb70-cc2c857f071b" />
# SQL Injection Vulnerability in WHERE Clause Allowing Retrieval of Hidden Data

## Vulnerability
SQL Injection (SQLi)

## Objective
Display products that are normally hidden by modifying the SQL query.

## Payload

```sql
' OR 1=1--
```

## Solution

1. Intercepted the request responsible for filtering products.
2. Identified that the category parameter was used in a SQL query.
3. Injected the payload:

```sql
' OR 1=1--
```

4. The condition became always true.
5. Hidden products were displayed successfully.

## Impact

An attacker can bypass application filters and access data that should not be visible.

## Result

Lab solved successfully.
