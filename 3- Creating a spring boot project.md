
![[Screenshot From 2025-08-01 10-27-46.png]]


## ✅ 1. **Spring Web**

### 🔧 Role:

- Ye dependency tumhein **REST APIs** banane deti hai using **Spring MVC**.
    
- Ye internally **Apache Tomcat** use karta hai as an embedded server.
    

### 🧠 Interview-Style Explanation:

> "Sir, Spring Web humein RESTful services banane ke liye controllers, endpoints aur request mapping functionalities provide karta hai. Iske zariye hum browser ya Postman se HTTP requests handle kar sakte hain. Ye by default Apache Tomcat ko embedded server ke roop me use karta hai."

---

## ✅ 2. **Lombok**

### 🔧 Role:

- Ye ek annotation-based library hai jo **boilerplate code** (like getters, setters, constructors) ko hatata hai.
    

### 🧠 Interview-Style Explanation:

> "Sir, Lombok ek Java library hai jo annotations ke zariye repetitive code ko automatically generate kar deta hai. Jese `@Getter`, `@Setter`, `@NoArgsConstructor`, `@AllArgsConstructor`, `@Builder`, etc. Ye development ko clean aur fast banata hai."

---

## ✅ 3. **Spring Data JPA**

### 🔧 Role:

- Ye dependency tumhein **relational databases (SQL)** ke saath kaam karne ke liye high-level abstraction deti hai.
    
- Ye **JPA specification** ko follow karti hai aur **Hibernate** ko use karti hai as implementation.
    
- Tum `JpaRepository` bana kar CRUD operations kar sakte ho bina SQL likhe.
    

### 🧠 Interview-Style Explanation:

> "Sir, Spring Data JPA ek abstraction hai jo JPA specification ka use karke Hibernate ke zariye relational databases ke saath kaam karti hai. Ye developer ko repository interfaces ke zariye data access operations karne deti hai — bina SQL query likhe."

---

## ✅ 4. **PostgreSQL Driver**

### 🔧 Role:

- Ye ek **JDBC driver** hai jo Java applications ko **PostgreSQL database** ke saath connect karta hai.
    

### 🧠 Interview-Style Explanation:

> "Sir, PostgreSQL JDBC Driver Java application ko PostgreSQL database ke saath interact karne deta hai using standard JDBC APIs. Ye driver Hibernate aur JDBC ke beech bridge ka kaam karta hai jab hum SQL operations perform karte hain."

---

## 🔁 How They Work Together (Flow Style):


Spring Data JPA
    ↓
JPA (specification)
    ↓
Hibernate (implementation of JPA)
    ↓
JDBC (real database interaction)
