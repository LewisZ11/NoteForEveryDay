#### Can you explain how ajax communicate with backend?

(main usage, request and handling response from server)

(1 send request to backend, using what object XMLHttpRequest)

(2 receive data from backend, in which 方式)

(3 error handling issues)

When a user interacts with a web page that uses Ajax, JavaScript code running in the user's web browser sends an HTTP request to a server-side script running on a web server. The server-side script processes the request and sends back a response in a format such as JSON, XML, or HTML.

The JavaScript code in the user's web browser then handles the response from the server and updates the web page dynamically, without requiring a page refresh. This allows the user to interact with the web page more quickly and seamlessly than would be possible with traditional web development techniques.

Ajax communicates with the backend through the XMLHttpRequest object, which is part of the browser's built-in JavaScript API. The XMLHttpRequest object allows the browser to send and receive HTTP requests and responses asynchronously. The browser can use this object to send data to the server, and receive data from the server, without reloading the entire web page.

#### If you want to retrieve information from two tables? What you do?

(The use of SQL (Structured Query Language) to retrieve data from a relational database.)

(The use of JOIN statements to combine data from two or more tables based on a common field or key)

(The types of JOIN statements, such as INNER JOIN, LEFT JOIN, and RIGHT JOIN, and when to use each type)

(The importance of specifying the desired columns and using aliases to distinguish between columns with the same name in different tables)

#### Do you know about spring transaction?

(what is transaction)

(spring way to implement transaction)

(configuration of transactional settings like isolation level and propagation behavior)

1. The concept of transactions in enterprise applications and the importance of transaction management.
2. The use of Spring's @Transactional annotation to define transactional boundaries around methods or classes.
3. The configuration of transactional settings, such as transaction isolation level and propagation behavior.
4. The use of Spring's declarative and programmatic transaction management approaches.

#### What is sql injection and how to deal with it?

SQL injection is a type of security vulnerability that can **occur when an attacker enters malicious SQL code into an application's input fields, such as a login form or a search bar.** **This code is then executed by the application's database without proper validation, allowing the attacker to perform unauthorized actions or retrieve sensitive information.**

To deal with SQL injection attacks, you can take the following steps:

1. Use parameterized queries: Instead of concatenating user input directly into SQL statements, use parameterized queries with placeholders to sanitize and validate user input. This technique prevents malicious SQL code from being executed by the database.

2. Limit privileges: Ensure that database users only have the necessary permissions to perform their required actions. This reduces the impact of a successful SQL injection attack.

3. Input validation: Validate all user input before processing it and ensure that it meets expected criteria. This includes ensuring that input is of the correct data type, length, and format.

4. Sanitize user input: Remove all special characters from user input, as they can be used to inject SQL commands.

5. Error handling: Properly handle any errors that occur during the application's execution, such as unexpected user input, database connection issues, or invalid queries.

6. Keep software updated: Regularly update the software and database management systems to ensure that any known vulnerabilities are patched.

By taking these steps, you can prevent SQL injection attacks and ensure the security and integrity of your application's data.

#### HTTPS

HTTPS stands for Hypertext Transfer Protocol Secure. It is a secure version of the standard HTTP protocol that is used for communication between a web server and a client, such as a web browser.

HTTPS works by **encrypting the data exchanged between the client and the server using an SSL (Secure Sockets Layer) or TLS (Transport Layer Security) certificate.** This encryption ensures that any sensitive information, such as passwords, credit card numbers, or other personal information, cannot be intercepted or accessed by unauthorized third parties.

In addition to providing encryption, HTTPS also provides authentication, ensuring that the client is communicating with the correct server and not a fraudulent one. It also helps prevent data tampering or modification during transmission, as the encrypted data cannot be modified without being detected.

HTTPS is commonly used by websites that require secure communication, such as e-commerce sites, banking sites, and social networking sites. Browsers often display a padlock icon in the address bar or show a green address bar to indicate that the connection is secure and that data exchanged with the website is encrypted.

#### How do you combine two objects? You can do it in js, javascript or jquery. 

To combine two objects in JavaScript or jQuery, you can use the Object.assign() method. This method creates a new object by copying the properties of one or more source objects to a target object. Here is an example:

```javascript
const obj1 = { 
  name: "John", 
  age: 25 
};

const obj2 = { 
  address: "123 Main St", 
  phone: "555-555-1234" 
};

const combinedObj = Object.assign({}, obj1, obj2);

console.log(combinedObj);
// Output: { name: "John", age: 25, address: "123 Main St", phone: "555-555-1234" }
```

In this example, we first define two objects `obj1` and `obj2`. We then use the `Object.assign()` method to create a new object `combinedObj` by combining the properties of `obj1` and `obj2`. The first argument to `Object.assign()` is an empty object, which serves as the target object for the copy operation. The subsequent arguments are the source objects whose properties are to be copied to the target object.

Note that if the same property exists in both source objects, the value from the second object will overwrite the value from the first object in the combined object. If you need to perform a deep merge of two objects (i.e., merge nested properties), you may need to use a library such as Lodash or Underscore.js.



#### How can you do verification of objects from frontend which is a json?For example, you have a object including {name: riverside, age: 20}, how do you make sure name is a string and age is an int? How do you make sure name is of length 10?

To verify the properties of a JSON object in a frontend application, you can use the following steps:

1. Parse the JSON object: Parse the JSON object using a built-in function like JSON.parse() or a third-party library like jQuery.parseJSON(). This will convert the JSON object into a JavaScript object that you can manipulate and verify.

2. Check the type of the properties: Use the typeof operator to check the type of the properties in the JavaScript object. For example, you can use typeof to check if the name property is a string and if the age property is a number. If the type of a property does not match your expectations, you can return an error message to the user.

3. Check the length of the name property: Use the length property to check the length of the name property. For example, you can check if the length of the name property is equal to or less than 10. If the length of the name property is longer than 10, you can return an error message to the user.

Here's an example code snippet that demonstrates these steps:

```
let jsonString = '{ "name": "riverside", "age": 20 }';
let jsonObject = JSON.parse(jsonString);

if (typeof jsonObject.name !== 'string') {
  console.error('name property is not a string');
}

if (typeof jsonObject.age !== 'number') {
  console.error('age property is not a number');
}

if (jsonObject.name.length > 10) {
  console.error('name property is too long');
}
```

By using these steps, you can verify the properties of a JSON object in a frontend application and ensure that they meet your requirements.

#### How stream differ from the member function on class? He said like we can use .map(), .filter() in the stream API, but we can also define these methods for the class, what makes stream different?

Streams and member functions on classes are different in several ways, even though they may have similar functionalities. Here are some of the differences:

1. Immutable vs. Mutable: Streams are designed to operate on immutable data, whereas member functions on classes operate on mutable data. Streams create new objects with each operation, rather than modifying the original object, which can help avoid unwanted side effects and improve performance in certain scenarios.

2. Chainable: Streams are designed to be easily chainable, which means that you can perform multiple operations on a stream in a single expression. This can make your code more concise and expressive. In contrast, member functions on classes typically do not support chaining in the same way.

3. Lazy Evaluation: Streams use lazy evaluation, which means that operations on a stream are not performed until they are needed. This can help reduce memory usage and improve performance in scenarios where not all elements in a stream need to be processed.

4. Composition: Streams allow for composition of operations, which means that you can combine multiple operations into a single expression to perform complex transformations on data. This can make your code more readable and easier to maintain.

5. Higher-Order Functions: Streams are built on higher-order functions, which means that they can take functions as arguments and return functions as results. This enables more flexible and dynamic processing of data.

In contrast, member functions on classes typically do not have these characteristics, and may be more limited in their functionality and flexibility. However, they can be useful in scenarios where you need to modify the state of an object directly or where you need more fine-grained control over the processing of data.

#### what is StreamApi ?

StreamAPI is a feature of Java that provides a way to process collections of objects in a declarative and functional style. It allows you to express complex data transformations and manipulations in a concise and readable way. The StreamAPI is designed to work with collections of objects, such as arrays or lists, and provides a set of methods that can be used to perform various operations on the data, such as filtering, mapping, and reducing.

#### If you write a functional interface with more than 1 abstract method, what will happen to the java compiler ?

If you write a functional interface with more than one abstract method, the Java compiler will generate an error. This is because a functional interface by definition can have only one abstract method, which is called the functional method or the single abstract method (SAM).

When the Java compiler encounters an interface that is annotated with the `@FunctionalInterface` annotation, it checks that the interface has only one abstract method. If the interface has more than one abstract method, the compiler will generate an error, indicating that the interface is not a valid functional interface.

For example, consider the following interface:

```java
@FunctionalInterface
public interface MyFunctionalInterface {
    void method1();
    void method2();
}
```

This interface has two abstract methods, `method1` and `method2`. When the Java compiler encounters this interface, it will generate an error, indicating that the interface is not a valid functional interface.

```
error: MyFunctionalInterface is not a functional interface
multiple non-overriding abstract methods found in interface MyFunctionalInterface
```

Therefore, it is important to ensure that any interface annotated with the `@FunctionalInterface` annotation has only one abstract method, to avoid compilation errors.

#### Why you want to use TreeMap ?

`TreeMap` is a class in Java that implements the `SortedMap` interface, which means that it maintains a sorted order of the elements in the map. The keys in a `TreeMap` are sorted according to their natural ordering or a custom comparator that is provided at the time of instantiation.

One of the main reasons to use a `TreeMap` is when you need to maintain a sorted order of the keys in a map. This can be useful in many scenarios, such as when you need to retrieve elements in a specific order, or when you need to perform range queries on the keys.

`TreeMap` provides several methods for accessing and manipulating the elements in the map, including methods for adding, removing, and retrieving elements, as well as methods for navigating the map and performing range queries.

Another advantage of using a `TreeMap` is that it provides guaranteed `O(log n)` time complexity for many operations, such as `put()`, `get()`, and `remove()`, which makes it suitable for large data sets.

However, `TreeMap` has a higher overhead than some other map implementations, such as `HashMap`, and may not be the best choice for scenarios where the order of the elements is not important, or where performance is a critical concern.

Overall, `TreeMap` is a useful class to use when you need to maintain a sorted order of the keys in a map and when performance is not a critical concern.

#### Let’s say we have a treemap<Employee, int>, what if we want to find an employee with a specific employee id?

If you have a `TreeMap` with keys of type `Employee` and values of type `int`, and you want to find the `Employee` object with a specific employee ID, you can use the following steps:

1. Create an instance of the `Employee` class with the employee ID you are looking for.
2. Use the `ceilingKey()` method of the `TreeMap` to find the smallest key greater than or equal to the key you are looking for.
3. If the key returned by `ceilingKey()` is not null, check if it matches the employee ID you are looking for. If it does, you have found the `Employee` object you are looking for. If it doesn't match, the `Employee` object you are looking for is not in the `TreeMap`.
4. If the key returned by `ceilingKey()` is null, the `Employee` object you are looking for is not in the `TreeMap`.

Here is some sample code that demonstrates this approach:

```java
// Assume we have a TreeMap<Employee, Integer> called employeeMap

int employeeId = 12345;
Employee searchKey = new Employee(employeeId);

Employee result = employeeMap.ceilingKey(searchKey);
if (result != null && result.getId() == employeeId) {
    // Found the Employee object with the specified ID
    int value = employeeMap.get(result);
    // Do something with the value
} else {
    // Employee object with specified ID not found
}
```

In this example, we create a new `Employee` object with the ID we are looking for, and use the `ceilingKey()` method to find the smallest key greater than or equal to this object. If the key returned by `ceilingKey()` is not null and its ID matches the one we are looking for, we have found the corresponding `Employee` object. If the key returned by `ceilingKey()` is null or its ID doesn't match, the `Employee` object we are looking for is not in the `TreeMap`.

#### In the production, if you find a bug in the product. How do you check log to find it? 

When you encounter a bug in a production environment, logs can be a valuable tool to help identify and diagnose the issue. Here are some steps you can take to check the logs:

1. Determine the log file location: Depending on the application or service, the logs may be stored in different locations. Check the configuration files or documentation to determine the location of the log files.

2. Identify the relevant log file: Once you have located the log files, identify the log file that contains the relevant information for the issue you are investigating. This may involve looking at timestamps or searching for specific keywords related to the issue.

3. Review the log entries: Open the log file and review the log entries for any errors or warnings that may be related to the issue. Look for any stack traces or error messages that provide additional context about the problem.

4. Use search or filtering tools: If the log file is very large, you may want to use search or filtering tools to narrow down the entries to those that are relevant to the issue you are investigating. Many text editors or command-line tools have built-in search or filtering capabilities that can be helpful.

5. Analyze the logs: Once you have identified the relevant log entries, analyze them to determine the root cause of the issue. Look for any patterns or correlations between the log entries and the symptoms of the problem.

6. Take action: Based on the information you have gathered from the logs, take appropriate action to address the issue. This may involve updating the application code, modifying the configuration, or making changes to the infrastructure.

In general, it is a good practice to log as much relevant information as possible in production environments, so that you can easily diagnose and troubleshoot issues when they arise. Additionally, you may want to consider implementing log aggregation and analysis tools to help automate the process of identifying and diagnosing issues in your production environment.

#### What are left join, right join in SQL?

In SQL, a join operation is used to combine rows from two or more tables based on a related column between them. A LEFT JOIN and RIGHT JOIN are two types of joins that combine rows from two tables in different ways.

A LEFT JOIN returns all the rows from the left table (also known as the "first" or "left-hand" table) and matching rows from the right table (also known as the "second" or "right-hand" table). If there are no matching rows in the right table, NULL values are returned for the columns of the right table.

#### if by default an HTTP request timeout in 5 minutes, but actually the backend needs 10 minutes to respond, what should you do. write code

If the backend needs more time to respond than the default timeout of an HTTP request, there are a few things you could do on the frontend:

1. Increase the timeout: You can increase the timeout for the HTTP request in the frontend code. This can be done by setting a longer timeout value when making the request. For example, in JavaScript, you can set the timeout in milliseconds like this:

```javascript
const timeout = 600000; // 10 minutes in milliseconds
fetch(url, { timeout })
  .then(response => {
    // Handle response
  })
  .catch(error => {
    // Handle error
  });
```

Note that not all HTTP clients have a timeout parameter that can be adjusted.

2. Implement a retry mechanism: If the backend is taking longer to respond than the default timeout, you can implement a retry mechanism in the frontend. This means that if the request times out, the frontend will automatically retry the request after a certain amount of time. For example, you can retry the request every minute until it succeeds or reaches a maximum number of retries.

3. Implement a loading indicator: If the backend is taking a long time to respond, you can display a loading indicator on the frontend to let the user know that the request is still in progress. This can help manage user expectations and prevent them from thinking that the application has crashed.

4. Optimize the backend: If the backend is consistently taking longer than the default timeout to respond, it may be necessary to optimize the backend code to reduce the response time.

Note that increasing the timeout should be done with caution, as it can have a negative impact on the user experience if the request takes too long to complete. In addition, if the backend is consistently taking longer than the default timeout, it may be an indication of a larger issue that needs to be addressed.

#### why String is immutable?

The question of why `String` is immutable is a common interview question for Java developers, particularly for those interviewing for mid-level or senior-level positions. The purpose of this question is to test the candidate's understanding of the reasons why `String` is designed as an immutable class in Java.

Here are some reasons why `String` is immutable:

1. Security: Immutable objects cannot be modified once they are created. This property is important for security because it prevents attackers from modifying strings that have been passed around between different parts of the program.

2. Thread-safety: Immutable objects are inherently thread-safe because they cannot be modified. This means that multiple threads can safely access and use the same `String` object without the risk of concurrency issues.

3. Performance: Immutability allows for certain optimizations in Java that can improve performance. For example, since `String` objects are immutable, they can be safely shared between different parts of the program without the need for defensive copying.

4. Cacheable: Immutable objects are often used as keys in hash tables and other collections because they can be cached safely. Since the hash code of an immutable object never changes, it can be calculated once and stored for later use.

When answering this interview question, it's important to demonstrate a clear understanding of these reasons and their significance for software development. Candidates should also be able to provide examples of how immutability is used in other Java classes, such as `BigInteger` and `BigDecimal`.

#### how to make class immutable ?

#### what change do you need to do in the pipeline when deploying an application on clouds?

When deploying an application on the cloud, there are several changes that you need to make to your deployment pipeline to ensure that the application is successfully deployed and can scale to meet demand. Here are some of the changes that you need to consider:

1. Infrastructure as Code: One significant change when deploying an application on the cloud is the use of Infrastructure as Code (IaC). IaC allows you to define the infrastructure of your application as code, making it easy to version control, test, and deploy. This approach ensures that your infrastructure is consistent, reproducible, and can be quickly scaled up or down.

2. Containerization: Containers provide a lightweight and portable way to package and deploy applications. When deploying on the cloud, containerization becomes a crucial part of the deployment pipeline. Containers can be quickly spun up, scaled out, and can be used to create a consistent runtime environment across multiple cloud platforms.

3. Automation and Orchestration: Cloud deployments require automation and orchestration tools to manage the entire deployment pipeline from code commit to production deployment. Tools like Jenkins, GitLab, and AWS CodeDeploy can be used to automate the building, testing, and deployment of your application.

4. Scalability and High Availability: Cloud platforms offer scalability and high availability capabilities that traditional on-premise deployments cannot match. You need to ensure that your application is designed to take advantage of these capabilities and can scale horizontally to handle spikes in traffic.

5. Monitoring and Logging: When deploying on the cloud, it is essential to have a robust monitoring and logging system in place to track application performance, detect issues, and troubleshoot problems quickly. Tools like Prometheus and ELK Stack can be used to collect, store, and analyze application metrics and logs.

In summary, deploying an application on the cloud requires changes to the deployment pipeline, including using IaC, containerization, automation, orchestration, scalability, high availability, and monitoring and logging. These changes will help ensure that your application is deployed quickly, reliably, and can scale to meet demand.

#### Spring Bean Life Cycle ?

The Spring framework manages the life cycle of beans through a series of callbacks, allowing you to perform operations at different stages of the bean's life cycle. The following are the different stages of the Spring bean life cycle:

1. Instantiation: At this stage, the Spring container creates an instance of the bean using the bean's class constructor.

2. Dependency Injection: After the bean is instantiated, the Spring container injects the dependencies (other beans or values) that are configured for the bean.

3. Initialization: Once the dependencies are injected, the Spring container invokes the `@PostConstruct` annotated method to perform any initialization tasks.

4. Usage: At this stage, the bean is ready to be used by the application.

5. Destruction: When the application context is closed, the Spring container destroys the beans by calling the `@PreDestroy` annotated method.

You can also define your own custom initialization and destruction methods using the `init-method` and `destroy-method` attributes in the bean configuration file.

Understanding the Spring bean life cycle is essential for developing and managing Spring applications, as it allows you to customize the behavior of the beans and perform any required operations at specific stages of the life cycle.

#### Spring Boot CLI ?

The Spring Boot CLI provides a command-line interface that allows you to quickly develop and test Spring Boot applications. Here are some commonly used Spring Boot CLI commands:

1. `spring run <filename.groovy>`: This command compiles and runs a Groovy script containing a Spring Boot application.

2. `spring init`: This command creates a new Spring Boot project with a specified set of dependencies. You can specify options such as project type, language, packaging, and dependencies.

3. `spring test`: This command runs tests in a Spring Boot application.

4. `spring shell`: This command starts a Spring shell, which is a command-line interface for interacting with a Spring application.

5. `spring jar`: This command creates a standalone executable JAR file for a Spring Boot application.

6. `spring help`: This command provides help on all Spring Boot CLI commands.

7. `spring install`: This command installs the Spring Boot CLI as a command-line tool on your local machine.

These are just a few of the many commands available in the Spring Boot CLI. The CLI is a powerful tool that can help you quickly develop and test Spring Boot applications, and it is worth exploring further to see how it can benefit your development workflow.