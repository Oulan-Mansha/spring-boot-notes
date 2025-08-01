


```
@Entity  
public class Patient {  
  
    @Id  
    @GeneratedValue(strategy = GenerationType.IDENTITY)  
    private Long id;   
}
```


### Entity

`@Entity` ek annotation hai jo batata hai:

> **"Yeh Java class database table ke barabar hai."**


### @Id

Primary key define karta hai.
**Primary Key** ka kaam hota hai **table ki har row ko uniquely identify karna.**

#### Rules of Primary Key:

|Rule|Meaning|
|---|---|
|🔹 Unique|Do rows ka primary key same nahi ho sakta|
|🔹 Not Null|Primary key kabhi bhi null nahi ho sakta|
|🔹 One per table|Har table mein sirf ek primary key hoti hai|
|🔹 Can be composite|Kabhi kabhi 2 ya zyada columns mil ke primary key bante hain (called **composite primary key**)|


### strategy


| Strategy   | Kya karta hai?                                                            | Kab use karein?               |
| ---------- | ------------------------------------------------------------------------- | ----------------------------- |
| `AUTO`     | Hibernate khud strategy choose karta hai                                  | Jab portable app banani ho    |
| `IDENTITY` | DB ka `AUTO_INCREMENT` use karta hai                                      | MySQL, PostgreSQL, SQL Server |
| `SEQUENCE` | DB ke andar sequence object hota hai jo har baar ek naya number deta hai. | PostgreSQL, Oracle            |
| `TABLE`    | Extra table banake IDs track karta hai.                                   | Har DB mein kaam karta hai    |
| `UUID`     | Random globally unique ID generate karta hai                              | Microservices, public IDs     |

|**Strategy**|**Kaam kaun karta hai?**|**Explanation (Simple Urdu)**|
|---|---|---|
|`AUTO`|Hibernate|Hibernate khud decide karta hai ke kaunsa use kare.|
|`IDENTITY`|**Database**|DB (jaise MySQL/PostgreSQL) khud `AUTO_INCREMENT` ya `SERIAL` se ID generate karta hai. Hibernate sirf wait karta hai.|
|`SEQUENCE`|**Database** (sequence) + Hibernate|Sequence DB mein hota hai, lekin Hibernate usse call karta hai aur ID assign karta hai.|
|`TABLE`|**Hibernate**|Hibernate ek table banaata hai jisme woh last ID store karta hai, DB ko koi idea nahi hota.|
|`UUID`|**Hibernate** (or Java code)|Hibernate ya Java random UUID generate karta hai. DB ka role nahi hota.|

> UUID = Universally Unique Identifier
> it is a 36 characters hexadecimal string

