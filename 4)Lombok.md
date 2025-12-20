# 🌶️ Project Lombok

**What is it?**
A Java library that helps you write less code. It automatically generates repetitive "boilerplate" code (like getters and setters) for you during compilation. 🛠️

**Why use it?**

* **Cleaner Code:** Your classes are shorter and easier to read. 📉
* **Saves Time:** You don't have to write or update standard methods manually. ⏱️

### 🔑 Key Annotations

| Annotation | Description |
| --- | --- |
| `@Getter` / `@Setter` | Automatically creates `getVariable()` and `setVariable()` methods. ↔️ |
| `@ToString` | Creates a method to print the object's data clearly. 📄 |
| `@EqualsAndHashCode` | Generates methods to compare objects correctly. ⚖️ |
| `@NoArgsConstructor` | Creates a constructor with **zero** arguments. 0️⃣ |
| `@AllArgsConstructor` | Creates a constructor with **all** arguments. 🔢 |
| `@Data` | **The Super Combo!** 📦 Includes `@Getter`, `@Setter`, `@ToString`, `@EqualsAndHashCode`, and `@RequiredArgsConstructor`. |
| `@Builder` | Allows you to create objects in a fluent way (e.g., `User.builder().name("John").build()`). 🧱 |
| `@Slf4j` | Gives you a logger instantly (e.g., `log.info("Hello")`). 🪵 |

### 📝 Example

**Without Lombok:** 😩

```java
public class User {
    private String name;
    
    public String getName() { return name; }
    public void setName(String name) { this.name = name; }
    // ... plus toString, hashCode, equals ...
}

```

**With Lombok:** 😎

```java
import lombok.Data;

@Data 
public class User {
    private String name;
    // That's it! Everything else is generated automatically. ✨
}

```