
###Html Tags

<main>     → main content of document

<section> → sections in a document such as chapters,headers,footers.

<header>   → heading elements,autorship information, etc.

<footer>   → contain information about about its container , element

**HTTP Verb** 	**CRUD** 
------------------------

- POST		Create
- GET		Read
- PUT 		Update
- DELETE	Delete

**REST** -> Representational State Transfer (REST) is a software architecture style for building scalable web services. RESTful systems typically, but not always, communicate over the Hypertext Transfer Protocol with the same HTTP verbs (GET, POST, PUT, DELETE, etc.) which web browsers use to retrieve web pages and to send data to remote servers.

Examples : 
```
	update?id=5         → request param (Servlet)
	update/5            → PathVariable  (Spring MVC)
	/update/{id}/{name} → (@PathVariable(“id”) Long id,(“name”) String name)
```
For example ; We use URL like update?id=5 in servlet project. But, we should change in the Spring MVC project. Besides, it doesn't fit the restful restrictions.

###PostgreSQL

* Installing Postgresql -> We should run some terminal codes in this sequence.

- sudo apt-get install postgresql-9.3
- sudo -u postgres createuser -D -A -P testuser
- sudo -u postgres createdb -O testuser testdb
- sudo apt-get install pgadmin3

Open pgAdmin and click add to new server, you should give your dB username and password. 
Now, you can find your tables under : databases -> testdb -> schemas -> public -> tables 

**@Valid** → Annotation if we want to valid a variable, we add this annotation on the variable.
create(@ModeAttribute @Valid Todo todo, Bindingresult bindingResult) //checks the valid

**ORM**    → (Object Relational Mapping) It converts data between RDBS to Object Oriented, so it is a programming technique. In this project, we use JPA(Hibernate) as an ORM.

JPA has a criteria API which creates the query. Example : 
```	
	Criteria criteria = this.createCriteria();
	criteria.add(Restrictions.in("id", ids));

	return criteria.list();
```
**Session** → is used to get a physical connection with a database.
 
**@Transaction** → annotation opens a session and inside this session makes the query. Otherwise, when the session is closed, doesn't save the changes of the object. We have to update these changes.

When the compiler sees these annotations, creates a copy one of them and adds this copy to the dependency pool.

- @Repository
- @Controller	
- @Service
- @Component
