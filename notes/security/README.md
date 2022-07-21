# 🐌 Security

Security is most important of Service.

<hr>

## Check List

- [?] Attacker should give same `{ key: value }` parameters?
- [?] Attacker should give some key words.
  - [] Check space bar %20


<hr>

## Pin Point

| Situation | Security Dangerous | Defense Strategy | Defense Strategy, Front |
| :-------- | :----------------- | :--------------- | :---------------------- |
| Use SQL   | [SQL Injection](https://www.hahwul.com/cullinan/sql-injection/)  | Prepare Statement, Input Validator | |
| Use NoSQL | [NoSQL Injection](https://www.hahwul.com/cullinan/nosql-injection/) | Protector of NoSQL | `sanitize-html`, module |
| Use Cookie | [CSRF, `Cross-Site Request Forgery`](https://www.hahwul.com/cullinan/csrf/#csrf-token) | Referer Check, Origin Check | CSRS Token(+ Host Prefix) 
| Use JWT | [Fake JWT](https://www.hahwul.com/cullinan/jwt/) | Expired Time, Sliding Session, Except Important Data | |
