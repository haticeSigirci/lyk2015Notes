
##Why do we prefer using Servlet instead of the Framework?

In the servlet, we have only two methods; doGet and doPost. Then we have to parse with if else structure because it does not have a structure according to the parameters coming from URLs directly.

###JSR303 Bean Validation

*JavaBeans Validation (Bean Validation)* is a new validation model available as part of Java EE 6 platform. The Bean Validation model is supported by constraints in the form of annotations placed on a field, method, or class of a JavaBeans component, such as a managed bean.
In the following example, a constraint is placed on a field using the built-in @NotNull constraint:
```
	@NotNull //Annotation
	private String name;	//initial value shouldn't null
```
You can also place more than one constraint on a single JavaBeans component object. For example, you can place an additional constraint for size of field on the firstname and the lastname fields:
```
	public class Name {
	    @NotNull
	    @Size(min=1, max=16)
	    private String firstname;

	    @NotNull 
	    @Size(min=1, max=16)
	    private String lastname;
	}
```
###Java Code Conventions

*Code conventions* improve the readability of the software, allowing engineers to understand new code more quickly and thoroughly.
Also you can see a pdf at the link [http://www.oracle.com/technetwork/java/codeconventions-150003.pdf]

*Convention over configuration* (also known as coding by convention) is a software design paradigm which seeks to decrease the number of decisions that developers need to make, gaining simplicity, and not necessarily losing flexibility.

*Pojo (Plain Old Java Object)* -> is an ordinary Java Object, not bound by any special restriction. POJO shouldn't have to any extends a class, implements an interface or constructor.

*JavaBean* is just a standard 
- All properties private (have getters and setters)
- A public default constructor
- Implements Serializable

###DependencyPool

All objects injected each other are gathered in here. Each object in dependency pool is singleton. Also, it works like static. 
Dependency Pool : UserDao , TxManager, Properties, Connection
UserDao(connection), TxManager(Properties) // dependent classes
Spring is used @Autowired, @Inject annotations.
CDI is used @Inject annotation.

UserDao object is produced by its dependent objects and it is pulled from the pool.

@Autowired
UserDao userDao; 

- **Reflection** -> In Java, normally private attributes can not access from other classes, but using reflection can access. Also, reflection dynamically call classes, methods, attributes, etc. at runtime.

Code example of this in Java (imagine the object in question is foo) :
```
	Method method = foo.getClass().getMethod("doSomething", null);
	method.invoke(foo, null);
```
###ThymeLeaf

Thymeleaf is xml/html/html5 template engine. It is used view layer in MVC. We integrated it with Spring MVC. Thymeleaf has own documentation. Link : [http://www.thymeleaf.org/doc/tutorials/2.1/thymeleafspring.pdf] (With Spring)

Above we have some thymeleaf usage examples;
```
	- th:href=”@{/css/main.css}” 
	- th:text=”#{home.welcome}” 

	- <div th:object=”${session.user}” >

	<p th:text=”*{name} /> or th:text=”${session.user.name}” 

	</div>

	- < a href=”details.html” th:href=”@{/order/details{orderID=${o.id}}}”>view </a>

	- <div th:if=”${user.isAdmin()==false}” >

	- <tr th:each=”user: $(users)”>

	<td th:text=${username}> Hatice </td> 
```
