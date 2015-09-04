##JSP## 

In this example project, Eclipse is used as an IDE and tomcat is downloaded and added Eclipse. First of all, we have got four URLs : new, list, index and test. To purpose this project to understand how to run server applications before start the using MVC. Our project keeps the lists of todo. We can add a new record, list existing records, storage records and create test records.

Index.jsp : just show the welcome message
New.jsp   : add new to-do Fields: Name, Desc, Date
List.jsp  : list to-do or update to-do as done if it does
Test.jsp  : create test data

###Our Java classes### 

- **Todo.java**        : Id, Counter, Name, Done, Desc,Date . 
- **TodoServlet.java** : We have two methods in this class; doGet and doPost(HTTP Methods). We send data for new.jsp in the doGet method. Our data were received from the form, is parsed and then new data was sent our todo object and this object is added our hashmap.
- **Storage.java**	 : This class was used like database. This class only keeps data inside a map. Also, this class is a static class in this way, our all class can use Storage class. Secondly, our change in Todo class is updated in Storage class. 
- **TestServlet.java** : We generate random data and add this data our list. In this way, we show our list.
- **ListServlet.java** : We view all data is received from the Storage class . Besides, data is updated from the id with a save button.

Example java classes : https://github.com/haticeSigirci/sampleservlet-lyk2015
