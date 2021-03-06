##CleanCode##

* Classes should start with a capital letter
* Methods should start with a small letter
* Field names should start with a small letter
* Lists should use plural names
* Use meaningful names
* Methods should be small
* Methods should only do one thing
* Encapsulate boolean expressions
* Avoid unclear/ambiguous class name
* Encapsulate overly-complex code
* Avoid deep nesting
* Keep each step simple
* Replace constructors with creation methods

##Dependency Injection##

Dependency injection(DI) is a design pattern that has several advantages. First of all, DI makes more flexible your code. In this way, testing your code is easier. There are various methods of dependency injection, in our project we use dependency injection with spring mvc. If we want to inject one class to another class, we added Autowired annotation on class name.
(For instance; 
@Autowired
protected TodoDao todoDao; )

- **MVC**          -> Model-View-Controller is a software arhitectural pattern. Each layer has own duties and this implementation is easier. Other implementations are more difficult because if we want to change some part of the code, it is more complicated. Besides, it is more understandable, systematic and well-organized.

- **Model** 	   -> Fields and methods (Business Logic)
- **View**  	   -> HTML, JSP, CSS, PDF, JavaScript -> not render yet
- **Controller**   -> Our decision mechanism is this layer. Produce a result for view layer

###How to work this mechanism ?###

FrontController Dispatcher Servlet -> Controller -> Model -> View -> HTML vs.

- **Service Layer** -> For instance, university of students should be control of his/her university. Such as check works should be in service layer.
- **Dao	Layer** -> This layer has one responsibility that is data transfer. 

- **SRP -Single Responsibility Principle-** -> Each object is responsible from one duty. Controller is responsible from basic control and redirections. 


