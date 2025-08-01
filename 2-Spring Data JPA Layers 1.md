
![[Screenshot From 2025-08-01 09-45-35.png]]




---

### 🔽 1. **JDBC (Java Database Connectivity)** – _Lowest Level_

> Ye sabse neeche wali layer hai jo **actual SQL queries database tak pohanchata hai aur wahan se result laata hai**. Ye Java ka low-level API hai database se direct communication ke liye.

---

### 🔽 2. **Hibernate** – _ORM (Object-Relational Mapping) Tool_

> Hibernate ek ORM tool hai jo **Java objects ko database tables ke rows me map karta hai aur vice versa**. Ye JPA specification ka implementation hai. Hibernate queries generate karta hai aur execution ke liye **JDBC ka use karta hai**.

---

### 🔽 3. **JPA (Java Persistence API)** – _Specification Layer_

> JPA ek **Java specification** hai jo define karti hai ke Java objects ko relational database se kaise map karna chahiye. Ye khud koi implementation nahi deta — iske liye Hibernate jaise tools use hote hain.

---

### 🔽 4. **Spring Data JPA** – _Top Abstraction Layer_

> Ye Spring framework ka hissa hai jo JPA ko aur simplify karta hai. Isme hum bas repository interfaces banate hain aur CRUD operations bina SQL likhe easily perform kar sakte hain. Ye internally JPA → Hibernate → JDBC ka use karta hai.

---

