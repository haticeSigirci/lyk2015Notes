###HTTP Status Code

**HTTP 1xx** -> Informational
**HTTP 2xx** -> Success
**HTTP 3xx** -> Redirection
**HTTP 4xx** -> Client Error
**HTTP 5xx** -> Server Error 

- Integer k → creates an object , assigns null as default
- int k → primitive data type , default value is zero

* UpdateForm should result new page with redirect because if user refresh the page , process is repeated. 

**Bootstrap** is the most popular HTML, CSS, and JavaScript framework for developing responsive, mobile-first web sites.

We have a Layout/main.html which is bootstrap css file. Besides we should include bootstrap.css and bootstrap.js in static directory.

```
	<head></head>

	<main>

	<th:block th:include=”<path>” > </th:block>

	th:include=<path>::fragement.name // <th:block th:include="${layout_main} :: content"

	<main th:fragment=”layout_content”> <div> test</div> </main>
```

**Interceptor** -> It is changed view that is given from controller, <th:include> is added and then is sent to view. If we don't want to guidance in the forward or redirect, intercepter can be handle this. So, we can change sequence with interceptor.

**Dispatcher Servlet -> Controller -> Model -> Interceptor -> View** 

##Forward vs Redirect

- **Forward**  -> The servlet container just forwards the same request to the target url, without the browser knowing about that. When the forward is done, the original request and response objects are transfered along with additional parameters if needed. (serverside)

- **Redirect** -> sets HTTP status to 302. The redirect sends a header back to the browser / client. This header contains the resource url to be redirected by the browser. Then the browser initiates a new request to the given url. Since it is a new request, the old request and response object is lost. (browserside)

