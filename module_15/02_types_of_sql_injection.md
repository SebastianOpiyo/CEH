# Section 02: Types of SQL Injection

## Types
- Types include
  - [In-band SQL injection](https://www.acunetix.com/blog/articles/sqli-part-4-in-band-sqli-classic-sqli/#:~:text=In-band%20SQL%20injection%20is%20the%20most%20common%20and,SQL%20injection%20are%20Error-based%20SQLi%20and%20Union-based%20SQLi.)
  - [Blind SQL injection](https://www.acunetix.com/blog/articles/sqli-part-5-inferential-sqli-blind-sqli/)
  - [Out-of-band SQL injection](https://www.acunetix.com/blog/articles/sqli-part-6-out-of-band-sqli/)
- Other classifications sometimes include
  - **Database management system-specific SQL injection**
    - Using specific SQL statements to certain database engine.
  - **Compounded SQL injection**
    - Combining SQL injection with other web application attacks such as • insufficient authentication • DDoS attacks • DNS hijacking • XSS.
    - E.g. DDoSing through `http://cloudarchitecture.io/azure?id=2 and WAITFOR DELAY '0:0:50'`
  - **Second-order SQL injection**
    - When user-supplied data is stored by the application and later incorporated into SQL queries in an unsafe way.
    - E.g. during login user name and password is retrieved as `WHERE username="$username" and password="$password"`, one could then set a password as `"); drop table users;` to delete the table and it will only executed during user login.
