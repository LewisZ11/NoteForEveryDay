#### How do you debug when client send a request to server but get many errors? 

(identify what is the error, check network connection issues, check error is reproducable)

(check the http request or response/test the api endpoints, to verify it is a client issue)

(check the server logs, find some of the exception issues, errors information here)

(check the server side code/use debug tools)

(cannot do it, finally seek help from others)

Debugging errors that occur when a client sends a request to a server can be a complex process, but there are some steps you can follow to help you identify and resolve the issue:

1. Identify the error messages: Take a closer look at the error messages that the client is receiving. Try to identify the patterns or similarities in the error messages. This can give you a clue as to what might be causing the issue.
2. Check the network connection: Ensure that the client has a stable and reliable network connection. If the connection is poor or unstable, it can cause errors when sending requests to the server.
3. Test the API endpoints: Test the API endpoints using a tool like Postman or cURL. This can help you identify if the issue is specific to a certain endpoint or if it's a more widespread issue.
4. Check the server logs: Check the server logs to see if there are any error messages or warnings that might be related to the issue. Look for any unusual patterns or events that might be causing the issue.
5. Check the server-side code: Check the server-side code to see if there are any bugs or errors that might be causing the issue. Look for any areas of the code that might be failing or throwing exceptions.
6. Use debugging tools: Use debugging tools to help identify the root cause of the issue. For example, you could use a debugger to step through the code and see where it's failing.
7. Seek help from others: If you're still having trouble identifying and resolving the issue, seek help from others. This might include colleagues or community forums where you can ask for advice and guidance.

By following these steps, you should be able to identify and resolve the issue that's causing the errors when the client sends a request to the server.

####  <font color="red">What are the general steps you should do if your system is normal but suddenly throws many error at 2 am? (He used many sentences to describe this question, but this is the main idea. I answered check logger & gave more details related to debugging, but he seems not satisfied)</font>

If your system suddenly throws many errors at 2 am, here are some general steps you can follow to identify and resolve the issue:

1. Check the system logs: Check the logs to see if there are any error messages or warnings that might be related to the issue. Look for any unusual patterns or events that might be causing the issue.

2. Check the network connection: Ensure that the system has a stable and reliable network connection. If the connection is poor or unstable, it can cause errors in the system.

3. Check for any recent changes: Check if any recent changes have been made to the system or any dependencies. This could include changes to the system configuration, code, or infrastructure.

4. Rollback recent changes: If you identify any recent changes that might be causing the issue, consider rolling back those changes to see if it resolves the problem.

5. Use debugging tools: Use debugging tools to help identify the root cause of the issue. For example, you could use a debugger to step through the code and see where it's failing.

6. Test the system: Test the system using a testing environment to replicate the issue and troubleshoot it in a controlled environment.

7. Seek help from others: If you're still having trouble identifying and resolving the issue, seek help from others. This might include colleagues or community forums where you can ask for advice and guidance.

In summary, when a system suddenly throws many errors, it's important to check the system logs, network connection, recent changes, use debugging tools, test the system, and seek help from others if needed. These steps can help you identify and resolve the issue quickly and effectively.

#### How do you use logger in your code ?

(import the logger library)

(set the logging level, config logging handlers)

(add logging message, customize the logging output)

(test the logger output)

Logging is an important tool for developers to help them debug and diagnose issues in their code. Here are some general steps to use logger in your code:

1. Import the logger library: Most programming languages come with a built-in logger library, which you can import at the beginning of your code.

2. Set the logging level: The logging level determines the severity of the messages that the logger will output. There are several logging levels available, such as DEBUG, INFO, WARNING, ERROR, and CRITICAL. You should set the logging level to the appropriate level based on the severity of the message.

3. Add logging messages: You can add logging messages throughout your code by using the appropriate logging method. For example, you might use logger.debug() to output a debug message, logger.info() to output an informational message, and logger.error() to output an error message.

4. Customize logging output: You can customize the output of the logging messages to include additional information, such as the current date and time, the name of the function that's being executed, and the thread ID.

5. Configure logging handlers: You can configure logging handlers to control where the logging messages are sent. For example, you might send logging messages to a file, to the console, or to a remote server.

6. Test logging output: Test the logging output to ensure that the messages are being outputted to the correct location and that they contain the appropriate information.

Overall, logging can be a powerful tool for developers to help them debug and diagnose issues in their code. By following these steps, you can use logging effectively in your code to help you identify and resolve issues quickly and efficiently.

#### what is SOLID 

#### design patterns used in the project (my answer includes singleton, builder) singleton, builder – how did you use in your project

#### how did you use multi-threading in your project ?

1. create a scheduled task (不重要：@EnableScheduling, @Scheduled on method)
2. fetch todays order information, send to KafKa and then delete today's order
3. statistics server receive today's order information, insert data into database. history_db
4. (reduce the amount of order information in database and thus improve effiency when system need to search today's order information)
5. this method is internally implemented by ScheduledThreadPoolExecutor

https://blog.csdn.net/qianlixiaomage/article/details/106599951

https://juejin.cn/post/6844903924936212494#heading-3

#### what is immutable class? 

#### do you know string pool? 

#### what is runnable

#### what is stream? what is it used for?

In Java, a stream is a sequence of elements that can be processed in a functional or declarative way. A stream is not a data structure, but a concept that allows you to process collections of data in a more efficient and concise manner than traditional loops.

Streams are used to process data in a more functional and declarative way, which can make your code more concise, readable, and maintainable. With streams, you can avoid writing complex loops and nested conditionals, and focus on the high-level logic of your code.

#### what is predicate?  what is it used for?

Predicate is a functional interface that represents a boolean-valued function that takes one argument and returns a boolean value. (test)

Predicates are used to test whether an object or a collection of objects meet certain criteria. 

#### what is checked exception ?

Checked exceptions are checked by the compiler at compile-time, which means that if a method throws a checked exception, the calling method must handle or propagate the exception.

throw 之后就会terminated 程序

#### what do you know about concurrent?

Concurrency refers to the ability of a program to perform multiple tasks simultaneously, or at least appear to do so. In Java, concurrent programming is supported through the use of threads, which are lightweight sub-processes that can run concurrently within a single process.

Here are some key concepts related to concurrency in Java:

1. Thread safety: Thread safety refers to the ability of a program to execute correctly and safely in a multi-threaded environment. In Java, thread safety can be achieved through proper synchronization of shared resources.

2. Synchronization: Synchronization is a mechanism used to ensure that only one thread at a time can access a shared resource. In Java, synchronization is implemented using the `synchronized` keyword and locks.

3. Thread communication: Thread communication refers to the ability of threads to exchange information or signals with each other. In Java, thread communication can be achieved through mechanisms such as wait/notify, blocking queues, and concurrent collections.

4. Thread pools: Thread pools are a mechanism for managing a group of threads that can be reused for multiple tasks. In Java, thread pools can be implemented using the `Executor` framework and related classes.

5. Concurrent collections: Concurrent collections are collections that can be safely accessed and modified by multiple threads concurrently. In Java, concurrent collections are provided by the `java.util.concurrent` package.

Concurrency is an important aspect of Java backend development, as it enables applications to handle multiple requests and tasks simultaneously. However, concurrency also introduces new challenges, such as thread safety and synchronization, that must be carefully managed to ensure that the application is correct and reliable.

#### What is Error ?

In Java, an `Error` is a type of `Throwable` that indicates a serious problem that should not be caught or handled by the application code. **Errors are typically used to indicate unrecoverable problems that are caused by the environment or system, rather than by the application code itself.**

Here are some examples of `Error` types in Java:

1. `OutOfMemoryError`: This error occurs when the Java Virtual Machine (JVM) runs out of memory and is unable to allocate more memory for new objects. This error typically indicates a serious problem with the system or application, and may require changes to the application or system configuration to resolve.

2. `StackOverflowError`: This error occurs when the call stack of a thread becomes too large and overflows. This error typically indicates a problem with the application code, such as a recursive function that does not terminate properly.

3. `NoClassDefFoundError`: This error occurs when the JVM is unable to find a required class at runtime. This error typically indicates a problem with the application or system configuration, such as a missing or incorrect classpath.

4. `LinkageError`: This error occurs when the JVM encounters a problem with linking a class or resource, such as a missing or incompatible library. This error typically indicates a problem with the application or system configuration.

Errors are typically not caught or handled by the application code, as they indicate serious problems that may require changes to the application or system configuration to resolve. Instead, errors are typically logged or reported to the user, and the application may terminate or enter a fail-safe mode to prevent further damage or data loss.

#### @Entity and @Table: difference? Used together?

In Java Persistence API (JPA), `@Entity` and `@Table` are annotations that are used to define a mapping between a Java class and a database table.

Here is the difference between `@Entity` and `@Table`:

- `@Entity`: This annotation is used to mark a Java class as a JPA entity. An entity is a lightweight object that represents a row in a database table. When an entity is persisted, its properties are mapped to columns in the table.

- `@Table`: This annotation is used to specify the name of the database table that is mapped to the entity. By default, the name of the table is the same as the name of the entity class. However, in some cases, it may be necessary to specify a different name for the table.

When `@Entity` and `@Table` are used together, the `@Table` annotation is used to specify the name of the database table that is mapped to the entity. For example, the following code defines an entity class named `Customer` that is mapped to a database table named `CUSTOMERS`:

```
@Entity
@Table(name = "CUSTOMERS")
public class Customer {
    // class code here
}
```

In this example, the `@Entity` annotation marks the `Customer` class as a JPA entity, while the `@Table` annotation specifies that the entity is mapped to a database table named `CUSTOMERS`.

Overall, `@Entity` and `@Table` are used together to define the mapping between a Java class and a database table in JPA. The `@Entity` annotation marks the class as a JPA entity, while the `@Table` annotation specifies the name of the database table that is mapped to the entity.

#### Bean Component

In Spring, `@Bean` and `@Component` are both used to define beans, which are objects that are managed by the Spring IoC (Inversion of Control) container. While both annotations can be used to create beans, they have different purposes and usage scenarios.

Here is a brief overview of the differences between `@Bean` and `@Component`:

- `@Bean`: This annotation is used to define a bean explicitly in a Java configuration class. The method that is annotated with `@Bean` returns the object that should be registered as a bean in the Spring IoC container. `@Bean` methods can take arguments and can be conditional, meaning that they are only executed if certain conditions are met.

- `@Component`: This annotation is used to mark a Java class as a Spring-managed component. Spring components are automatically detected by the Spring IoC container and registered as beans. Components can be annotated with more specific annotations, such as `@Service`, `@Repository`, or `@Controller`, depending on their purpose.

So, why would you choose to use `@Component` instead of `@Bean`? Here are a few reasons:

- `@Component` is more concise: If you have a simple component that doesn't require any custom configuration, you can use `@Component` to define it in a single line of code, rather than creating a separate configuration class with a `@Bean` method.

- `@Component` supports automatic scanning: Spring can automatically detect and register components that are annotated with `@Component`, without the need for any explicit configuration. This can be useful for large applications that have many components.

- `@Component` provides a clear separation of concerns: By marking a class as a component, you are explicitly stating that it is a Spring-managed object that has a specific purpose within the application.

In summary, while both `@Bean` and `@Component` can be used to define beans in Spring, they have different purposes and usage scenarios. `@Bean` is used to define beans explicitly in a Java configuration class, while `@Component` is used to mark a Java class as a Spring-managed component that can be automatically detected and registered by the Spring IoC container.

#### do you have experience in cloud such as AWS?

As a Full Stack Developer, I have experience working with cloud platforms like AWS. I have worked with AWS to deploy and manage web applications, databases, and other cloud-based services. Specifically, my experience includes:

1. EC2 (Elastic Compute Cloud): I have worked with EC2 instances to deploy web applications and services. I have configured and launched instances, configured security groups, and monitored performance.

2. S3 (Simple Storage Service): I have used S3 to store and manage data, such as images, files, and backups. I have configured buckets, set up access control, and managed data lifecycle.

3. RDS (Relational Database Service): I have used RDS to deploy and manage relational databases. I have configured database instances, set up backups, and performed tuning and optimization.

4. Lambda: I have used Lambda to deploy serverless applications and functions. I have written code in languages like Python and Node.js, and deployed functions that are triggered by events.

5. API Gateway: I have used API Gateway to manage and deploy APIs. I have created APIs, set up routes, and configured authorization and authentication.

In addition to these services, I have also worked with other AWS services like CloudFront, CloudWatch, Route 53, and more. I am comfortable working with AWS and can quickly adapt to new services as needed.

#### what is Unit Testing? How to write unit tests?

Unit testing is a software testing technique that is used to test individual units or components of a software application. The main goal of unit testing is to verify that each unit or component of the application is working as expected and meets the specified requirements. It involves writing and executing test cases for each unit or component in isolation from the rest of the application.

Here is how I use unit testing in my development process:

1. Writing unit tests: I write unit tests for each individual unit or component of the application, using a testing framework like JUnit or Mockito. I ensure that the tests are covering all possible scenarios and edge cases.

2. Running unit tests: Once the unit tests are written, I run them to verify that each unit or component is working as expected. I use an automated testing tool like Jenkins or Travis CI to run the tests automatically every time there is a code change.

3. Fixing failing tests: If any unit test fails, I investigate the issue and fix the code to make the test pass. This ensures that any issues are caught early in the development process.

4. Refactoring code: If necessary, I refactor the code to improve the quality and maintainability of the application. I make sure that the unit tests are still passing after the refactoring.

5. Integrating with other tests: Once all the unit tests are passing, I integrate them with other types of tests like integration tests and end-to-end tests to verify the overall functionality of the application.

Overall, using unit testing in my development process helps me catch issues early and ensures that each unit or component of the application is working as expected. This leads to a more reliable and maintainable application.

#### what is the Lifecycle of development for your project ?

The lifecycle of development for my project generally follows the Agile development methodology, which consists of several stages. Here is an overview of the lifecycle of development for my project:

1. Planning: In this stage, we identify the goals of the project, define the scope of work, and gather requirements from stakeholders. We also create a project plan that outlines the timeline and resources required to complete the project.

2. Design: In this stage, we create a design for the application, including the architecture, data models, and user interfaces. We also identify the technologies and frameworks that will be used to implement the design.

3. Development: In this stage, we begin to implement the design, building the application feature by feature. We use an iterative approach, with each iteration consisting of several development sprints. During each sprint, we focus on developing and testing a specific set of features.

4. Testing: In this stage, we test the application to ensure that it meets the requirements and is free from bugs and errors. We use a variety of testing techniques, including unit testing, integration testing, and end-to-end testing.

5. Deployment: In this stage, we deploy the application to a staging environment for further testing and validation. Once the application is stable and meets the requirements, we deploy it to production.

6. Maintenance: In this stage, we maintain and support the application, fixing bugs and adding new features as needed. We also monitor the application for performance and security issues and take action to prevent or resolve any problems that arise.

Throughout the development lifecycle, we work closely with stakeholders and end-users to ensure that the application meets their requirements and delivers value. We also continuously monitor and evaluate the performance of the application and use feedback to improve the product and development process.
