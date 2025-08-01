
| Strategy   | Kya karta hai?                               | Kab use karein?               |
| ---------- | -------------------------------------------- | ----------------------------- |
| `AUTO`     | Hibernate khud strategy choose karta hai     | Jab portable app banani ho    |
| `IDENTITY` | DB ka `AUTO_INCREMENT` use karta hai         | MySQL, PostgreSQL, SQL Server |
| `SEQUENCE` | Sequence object use karta hai                | PostgreSQL, Oracle            |
| `TABLE`    | Extra table banake IDs track karta hai.      | Har DB mein kaam karta hai    |
| `UUID`     | Random globally unique ID generate karta hai | Microservices, public IDs     |