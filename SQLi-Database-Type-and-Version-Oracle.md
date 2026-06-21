# SQL Injection Attack, Querying the Database Type and Version on Oracle

## Vulnerability
SQL Injection (SQLi)

## Objective
Determine the database type and retrieve its version information.

## Payload

```sql
' UNION SELECT banner, NULL FROM v$version--
```

## Solution

1. Identified a SQL Injection vulnerability in the product category parameter.
2. Determined the number of columns using ORDER BY and UNION attacks.
3. Found columns compatible with string data.
4. Queried Oracle version information using:

```sql
' UNION SELECT banner, NULL FROM v$version--
```

5. Retrieved database version details from the Oracle system table.

## Impact

An attacker can gather information about the backend database, which can help in planning further attacks.

## Result

Successfully identified the database as Oracle and retrieved version information.
