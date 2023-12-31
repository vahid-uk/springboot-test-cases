## springboot-test-cases

## standalone JUnit
> JUnit competes against spock and TestNG

JUnit can be used to separate out test cases use @Before to configure reuse / requirements. 
It separates testing code from source code and integrate with CI, Ant and Maven. 
You can arrange, ignore test cases and has a wide range of Assert methods such as 
assertEquals assertSame

---

## standalone JUnit with Mock
Using mocks and stubs allows developer to focus on the test module. Using mock data you can setup 
correct fixture, and focus on the test module logic.

---

## Spring MVC or Spring Data Test
With the @DataJpaTest annotation, Spring Boot provides a convenient way to set up an 
environment with an embedded database to test our database queries against.

@WebMvcTest : annotation is only to instantiates only the web layer rather 
than the whole context, so all dependencies in controller class should be mocked, 
covered in [documentation](https://spring.io/guides/gs/testing-web/)

Spring Boot instantiates only the web layer rather than the whole context. 
In an application with multiple controllers, you can even ask for only one to be instantiated 
by using, for example, @WebMvcTest(HomeController.class).

We use @MockBean to create and inject a mock for the services (if you do not do so, 
the application context cannot start)

---

##  Spring Boot test
Spring boot test annotation actual load the application context for test environment

The @SpringBootTest annotation tells Spring Boot to look for a main configuration class 
(one with @SpringBootApplication, for instance) and use that to start a Spring application context.

---

#### DB Console

> http://localhost:8080/h2-console
--

#### Actions:

> http://localhost:8080/
 
> http://localhost:8080/?name=Test
 
> http://localhost:8080/greeting
 
> http://localhost:8080/greeting?name=Test
 
> http://localhost:8080/sum
 
> http://localhost:8080/sum?val1=2&val2=2

Change variables accordingly