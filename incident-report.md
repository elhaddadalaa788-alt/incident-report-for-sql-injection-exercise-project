# Incident Report: SQL Injection Vulnerability

## Introduction
This report documents a SQL Injection vulnerability identified using DVWA in a controlled lab environment.

## Incident Description
A SQL Injection vulnerability was discovered in the user ID input field of the DVWA application. The input was not properly validated, allowing malicious SQL queries to be executed.

## Reproduction Process
1. Logged into DVWA as admin.
2. Set security level to Low.
3. Navigated to the SQL Injection module.
4. Entered the payload: `1' OR '1'='1`
5. Submitted the request and observed database output.

## Incident Impact
This vulnerability allows attackers to retrieve sensitive user data from the database without authentication.

## Recommendations
- Use prepared statements.
- Validate and sanitize user input.
- Apply least privilege principles to database users.

## Conclusion
SQL Injection vulnerabilities can lead to serious data exposure. Proper input handling and secure coding practices are essential to prevent such attacks.
