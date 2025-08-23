This will include:

Core Java concepts Q&A

OOPs, Collections, Exception handling

Coding/Problem-solving questions (with code examples)

Most asked HR-style Java programming questions for freshers at Capgemini, TCS, Infosys, Wipro, etc.

📌 Java Programming Interview Q&A (Fresher-Friendly)
🟢 Core Java Basics

1. What are features of Java?

Object-oriented, Platform-independent (JVM), Simple, Secure, Robust, Multithreaded.

2. What is the difference between JDK, JRE, and JVM?

JDK: Development kit (compiler + tools).

JRE: Runtime environment.

JVM: Executes Java bytecode.

3. What is the difference between == and .equals() in Java?

==: Compares references (memory addresses).

.equals(): Compares values (content).

4. Why is Java platform independent?

Java code compiles to bytecode, which JVM executes on any OS.

5. What is the difference between final, finally, and finalize()?

final: Keyword (constant, cannot inherit/override).

finally: Block in exception handling (always executes).

finalize(): Method called by Garbage Collector before destroying object.

🟠 OOPs Concepts

6. What are the four pillars of OOP in Java?

Encapsulation, Inheritance, Polymorphism, Abstraction.

7. What is method overloading vs method overriding?

Overloading: Same method name, different parameters (Compile-time polymorphism).

Overriding: Child class provides new implementation for parent method (Runtime polymorphism).

8. Can Java support multiple inheritance?

No (with classes), Yes (with interfaces).

9. What is the difference between Abstract class and Interface?

Abstract class: Can have both abstract & concrete methods.

Interface: Only abstract methods (Java 8 → default & static methods allowed).

10. What is encapsulation in Java?

Wrapping data + methods together. Achieved using private variables + getters/setters.

🔵 Java Collections

11. What is the difference between List, Set, and Map?

List: Ordered, allows duplicates (ArrayList, LinkedList).

Set: No duplicates (HashSet, TreeSet).

Map: Key-value pairs (HashMap, TreeMap).

12. Difference between ArrayList and LinkedList?

ArrayList: Fast for random access.

LinkedList: Fast for insert/delete operations.

13. Difference between HashMap and Hashtable?

HashMap: Not synchronized, faster.

Hashtable: Synchronized, slower.

14. How does HashMap work internally?

Stores data in buckets using hashcode() & equals().

15. What is the difference between Iterator and ListIterator?

Iterator: Forward only.

ListIterator: Forward & backward.

🔴 Exception Handling

16. What is the difference between checked and unchecked exceptions?

Checked: Compile-time (IOException).

Unchecked: Runtime (NullPointerException).

17. What is the difference between throw and throws?

throw: Used to throw exception.

throws: Declares exceptions a method may throw.

18. Can finally block be skipped?

Yes, if System.exit() is called before it.

19. Can you write try block without catch?

Yes, but must have finally.

20. What are custom exceptions in Java?

User-defined exceptions extending Exception class.

⚡ Multithreading

21. What is the difference between process and thread?

Process: Independent program.

Thread: Lightweight unit inside process.

22. How do you create a thread in Java?

By extending Thread or implementing Runnable.

23. What is synchronization in Java?

Prevents multiple threads from accessing shared resource simultaneously.

24. What is deadlock in Java?

Two threads waiting for each other, blocked forever.

25. What is the difference between sleep() and wait()?

sleep(): Temporarily pauses thread, doesn’t release lock.

wait(): Releases lock, waits until notify().

🟣 Java Coding Questions (For Freshers)

26. Write a Java program to check if a number is prime.

class PrimeCheck {
    public static void main(String args[]) {
        int n = 29, flag = 0;
        for(int i = 2; i <= n/2; i++) {
            if(n % i == 0) { flag = 1; break; }
        }
        if(flag == 0) System.out.println("Prime");
        else System.out.println("Not Prime");
    }
}


27. Write a Java program to reverse a string.

class ReverseString {
    public static void main(String[] args) {
        String str = "Java";
        String rev = "";
        for(int i=str.length()-1; i>=0; i--)
            rev += str.charAt(i);
        System.out.println(rev);
    }
}


28. Write a Java program to check palindrome.

class Palindrome {
    public static void main(String[] args) {
        String str = "madam";
        String rev = new StringBuilder(str).reverse().toString();
        if(str.equals(rev))
            System.out.println("Palindrome");
        else
            System.out.println("Not Palindrome");
    }
}


29. Write a Java program for Fibonacci series.

class Fibonacci {
    public static void main(String[] args) {
        int n = 10, a = 0, b = 1;
        System.out.print(a + " " + b);
        for(int i=2; i<n; i++) {
            int c = a + b;
            System.out.print(" " + c);
            a = b; b = c;
        }
    }
}


30. Write a Java program to find factorial.

class Factorial {
    static int fact(int n) {
        if(n==0) return 1;
        return n * fact(n-1);
    }
    public static void main(String[] args) {
        System.out.println(fact(5));
    }
}


31. Java program to find largest element in array.

class LargestInArray {
    public static void main(String[] args) {
        int arr[] = {10, 4, 23, 56, 1};
        int max = arr[0];
        for(int i=1; i<arr.length; i++)
            if(arr[i] > max) max = arr[i];
        System.out.println("Largest: " + max);
    }
}


32. Java program to sort an array.

import java.util.Arrays;
class SortArray {
    public static void main(String[] args) {
        int arr[] = {5,2,8,1,3};
        Arrays.sort(arr);
        for(int i: arr) System.out.print(i + " ");
    }
}


33. Java program to swap two numbers without third variable.

class Swap {
    public static void main(String[] args) {
        int a=5, b=10;
        a = a+b;  
        b = a-b;  
        a = a-b;  
        System.out.println("a="+a+", b="+b);
    }
}


34. Java program to count vowels in a string.

class CountVowels {
    public static void main(String[] args) {
        String str = "Interview";
        int count = 0;
        for(char c: str.toLowerCase().toCharArray()) {
            if("aeiou".indexOf(c) != -1) count++;
        }
        System.out.println("Vowels: " + count);
    }
}


35. Java program to check Armstrong number.

class Armstrong {
    public static void main(String[] args) {
        int n = 153, sum=0, temp=n;
        while(n > 0) {
            int r = n % 10;
            sum += r*r*r;
            n /= 10;
        }
        if(temp == sum) System.out.println("Armstrong");
        else System.out.println("Not Armstrong");
    }
}

🔥 Other Common Fresher Java Questions

36. What is String immutability in Java?

Once created, a String cannot be changed → new object created if modified.

37. Difference between String, StringBuffer, and StringBuilder?

String: Immutable.

StringBuffer: Mutable, synchronized.

StringBuilder: Mutable, not synchronized, faster.

38. Why is main() method static in Java?

JVM calls main() without creating object.

39. What is the difference between static and instance variables?

Static: Shared across all objects.

Instance: Unique per object.

40. Difference between this and super?

this: Refers to current object.

super: Refers to parent class.

41. Can we overload main() method?

Yes, but JVM always calls public static void main(String[] args).

42. What is constructor chaining?

Calling one constructor from another in same class (using this()) or parent class (super()).

43. What is garbage collection in Java?

Automatic memory management by JVM.

44. Difference between shallow copy and deep copy?

Shallow: References same object.

Deep: Creates a new object with copied values.

45. Difference between == and equalsIgnoreCase() in strings?

==: Compares references.

equalsIgnoreCase(): Compares values ignoring case.

46. Can a constructor be private?

Yes (used in Singleton pattern).

47. What is Singleton class in Java?

Only one instance allowed.

48. Example of Singleton class?

class Singleton {
    private static Singleton instance;
    private Singleton() {}
    public static Singleton getInstance() {
        if(instance == null) instance = new Singleton();
        return instance;
    }
}


49. What is the difference between compile-time error and runtime error?

Compile-time: Detected by compiler.

Runtime: Occurs during execution.

50. What is difference between interface and abstract class (short)?

Interface: 100% abstract (till Java 7).

Abstract: Can have both abstract and concrete methods.

✅ This gives you 50 Java fresher questions:

20 Conceptual (Core Java, OOP, Collections, Exceptions, Threads)

15 Coding questions (with programs)

15 HR-style + Project-related

👉 Do you want me to compile these into a neat PDF (with short answers + code) for your final-day interview revision?

You said:
and give advance java question also with answer
ChatGPT said:

Excellent 👍 You already have Core Java + Fresher coding Q&A, now let’s go deeper into Advanced Java Q&A.
For fresher/intermediate interviews (like Capgemini, TCS, Infosys, Wipro, Cognizant), “Advanced Java” usually means:

JDBC (Database connectivity)

Servlets & JSP

Hibernate & JPA basics

Spring Framework basics

Web services (REST, SOAP)

J2EE concepts

📌 Advanced Java Interview Questions (with Answers)
🟢 JDBC (Java Database Connectivity)

1. What is JDBC?

Java API for connecting and executing queries on a database.

2. What are the steps to connect Java to a database using JDBC?

Load driver class → Class.forName("com.mysql.cj.jdbc.Driver");

Establish connection → DriverManager.getConnection(...)

Create statement → Statement stmt = con.createStatement();

Execute query → ResultSet rs = stmt.executeQuery("SELECT * FROM users");

Close connection.

3. Difference between Statement and PreparedStatement?

Statement: Executes simple SQL (not safe).

PreparedStatement: Precompiled, prevents SQL injection.

4. Example of PreparedStatement in JDBC?

PreparedStatement ps = con.prepareStatement("SELECT * FROM users WHERE id=?");
ps.setInt(1, 101);
ResultSet rs = ps.executeQuery();


5. What is ResultSet in JDBC?

Represents query result (rows).

🟠 Servlets & JSP

6. What is a Servlet?

A Java class that handles HTTP requests & responses in web apps.

7. Servlet lifecycle?

init() → Called once.

service() → Handles request/response.

destroy() → Called before removal.

8. Difference between doGet() and doPost()?

doGet(): Sends data via URL, limited length.

doPost(): Sends data in request body, secure.

9. What is JSP (JavaServer Pages)?

Extension of Servlets, allows embedding Java code in HTML (<% %>).

10. Difference between JSP and Servlet?

JSP: HTML-centric with Java inside.

Servlet: Java-centric with HTML inside.

🔵 Hibernate & JPA

11. What is Hibernate?

An ORM (Object Relational Mapping) framework in Java.

12. Advantages of Hibernate?

No need for SQL (use HQL).

Database independent.

Caching for performance.

13. What is HQL?

Hibernate Query Language → object-oriented queries.

14. Example of Hibernate code?

Session session = factory.openSession();
Transaction tx = session.beginTransaction();
User u = new User(101,"Arihant");
session.save(u);
tx.commit();


15. Difference between Hibernate and JDBC?

JDBC: Manual SQL queries.

Hibernate: ORM framework → auto SQL generation.

🟡 Spring Framework

16. What is Spring Framework?

A lightweight Java framework for enterprise applications.

17. What is Dependency Injection (DI)?

Spring manages object creation instead of new.

18. What is the difference between Spring and Spring Boot?

Spring Boot: Simplifies configuration, embedded server, production-ready.

19. What is @Autowired in Spring?

Annotation to automatically inject dependencies.

20. What is Spring MVC?

A web framework in Spring → follows Model-View-Controller architecture.

🔒 Web Services

21. What are Web Services in Java?

Services that allow communication between applications over a network.

22. Difference between SOAP and REST web services?

SOAP: XML-based, strict, slower.

REST: Lightweight, uses HTTP, JSON/XML.

23. Example of REST API call in Java (Spring Boot)?

@GetMapping("/users/{id}")
public User getUser(@PathVariable int id) {
   return userRepo.findById(id).get();
}


24. What is JAX-RS in Java?

Java API for building RESTful web services.

25. What is JSON and why is it used?

Lightweight data format → used in REST APIs for communication.

⚡ J2EE Concepts

26. What is J2EE?

Java 2 Platform, Enterprise Edition → used for large-scale enterprise applications.

27. Difference between Core Java and Advanced Java?

Core Java: Basics, OOP, Collections.

Advanced Java: JDBC, Servlets, JSP, Hibernate, Spring, Web Services.

28. What is an EJB (Enterprise Java Bean)?

Server-side component used in enterprise apps (now less common, replaced by Spring).

29. What is JNDI in Java?

Java Naming and Directory Interface → lookup service for resources (DB, EJBs).

30. What is JMS in Java?

Java Messaging Service → for async communication between components.

🎯 Project/Scenario Questions (Advanced Java)

31. How did you use JDBC in your project (GeoVendor)?

Used JDBC to connect to MySQL database for storing vendor details.

32. How do you manage sessions in Servlets?

Using HttpSession session = request.getSession();

33. How do you prevent SQL Injection in JDBC?

By using PreparedStatement instead of Statement.

34. If multiple users login to your web app, how does Java handle requests?

Each request handled in a separate thread by the server (Tomcat).

35. Which design patterns did you use in your project?

MVC (Model-View-Controller) → Servlet (controller), JSP (view), JDBC/DAO (model).

36. How do you handle exceptions in Servlets?

Using try-catch + custom error pages in web.xml.

37. How would you secure your Java web app?

Use HTTPS (SSL/TLS), hashed passwords, session timeout.

38. How does Hibernate improve database performance?

By caching queries and reducing SQL queries.

39. How do you consume REST API in Java?

Using HttpURLConnection, RestTemplate (Spring).

40. Which servers can run Servlets?

Apache Tomcat, JBoss, Glassfish.

🔥 Coding Qs (Advanced Java Style)

41. Write JDBC code to insert data into MySQL.

Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/test","root","pass");
PreparedStatement ps = con.prepareStatement("INSERT INTO users VALUES (?, ?)");
ps.setInt(1, 101);
ps.setString(2, "Arihant");
ps.executeUpdate();


42. Write a simple Servlet example.

@WebServlet("/hello")
public class HelloServlet extends HttpServlet {
  protected void doGet(HttpServletRequest req, HttpServletResponse res) throws IOException {
      res.getWriter().println("Hello, World!");
  }
}


43. Write Hibernate code to fetch all users.

Session session = factory.openSession();
List<User> list = session.createQuery("from User").list();
for(User u : list) System.out.println(u.getName());


44. Write Spring Boot REST Controller.

@RestController
public class UserController {
    @GetMapping("/hello")
    public String sayHello() {
        return "Hello World";
    }
}


45. Write code to consume REST API in Java.

URL url = new URL("https://jsonplaceholder.typicode.com/posts/1");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
BufferedReader in = new BufferedReader(new InputStreamReader(con.getInputStream()));
String inputLine;
while ((inputLine = in.readLine()) != null) {
    System.out.println(inputLine);
}
in.close();
