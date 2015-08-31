##JAVA SE##

Today, we can continue with JavaSE lectures. In Java, package names are defined with domain name plus project name. In our example, "tr.org.kamp" is our domain name and is determined the whose project. “tr.org.kamp.spring” is our sub project.

Multiple interface cannot be allowed in Java,but we can apply this logic. All methods in our interface are abstract by default. You can find an example here : https://github.com/teaddict/lyk2015-Assessment

If we use final keyword, we cannot change the value of this variable. Also, we cannot override this method, so we can use only as a constant.
Static keyword; can be used to refer the common property of all objects. It gets only once in the class area at the time of class loading.

Generics enable types (classes and interfaces) can be used for several reasons such as elimination of casting, duplication of codes in classes.

###GIT###

We go to the our directory and then make the gitignore which include our name of the files.
You should use git commands in this sequence.

1. git init 			 -> We use when we first opened git repository
2. git status			 -> We can control to the changing files
3. git add . or git add --all    -> We add changing files in git repository
4. git commit -m "example commit"-> We save our changing
5. git push -u origin master     -> Finally,push all files in ourrepository

- **Authentication** : When we open the browser, each site has unique cookie for all information about this site keep in this cookie. In this way, even if we don't open a site, these cookies recognize us. 
Every site has "sessionID:object" pair. Actually, each item has a key and a value pair like a dictionary. We can access the objects of this site with this id.

- **Servlet** : Web server applications. Basically servlets are usually used to implement web applications. Servlets are Java classes based on the results from the web server requests.
User (get some request from the server) -> Server (decides which servlet is responsible for this request) -> Servlet (produces a final file) -> Result (send to the final server)-> Server -> User 

###Get/Post Methods ###

- **Get**  : Requests data from a specified resource
- **Post** : Submits data to be processed to a specified resource
