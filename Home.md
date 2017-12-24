Welcome to the JSP-Basics wiki!


### lanuage:

<%page language="java"%>

### import:
<%@ page import="java.sql.*,"java.util.*"%>

### info:
<%@ page ingo="this is the home page"%>

### extends:
<%@ page extends="com.pluralsight.demos"%>

### contenttype:
<%@page contentType="text/html"%>

### java standard tag library:
expression language
using custom tags
build a project

### model1:
developmetn will be easy and faster
Browser->request->jsp-->Data

### model2:
model->view->controller
business logic

servlet->controller
jsp->view
model->java bean


### expression tag:
<%=%>

### Declaration tag:
<% %>

`<%!`
`double getBonus(double salary)`
`{`
`return salary * 0.5;`
`}`
`%>`

<p>salary 5000 rs<%=getBonus(5000)%>

### 3->scriptlet tag:

`<%`
`for(int i=1;i<n;i++)`
`{`
`out.println(i+"<br>");`
`}`
`%>`


### -->Directives:

* @page Directive:
* <@page attribute="value" attribute="value" %>

* <@page language="java"%>
* <@page import="java.io.*"%>
* <@page language="java.sql.*"%>

* language:<@page language="java"%>
* import:<@page import="java.sql.*"%>
* info:<@page info="false"%>
* extends:<@page extends="false"%>
* contentType:<@page contentType="text/html"%>
* isELIgnored:
* isThreadSafe:<@page is ThreadSafe="false"%>
* pageEncoding:<@page pageEncoding="false"%>
* session:<@page session="false"%>
* buffer:<@page buffer="10kb"%>
* autoFlush:<@page autoFlush="true|false"%>

bootstrap:
CDN->CONTENT DELIVERY NETWORK


INCLUDE DIRECTIVE:
 ->read the specific file and merges its content into the jspp source code

<%@ include file="header.jsp"%>
<%@ include file="footer.jsp"%>

codesnippet.jsp

<% int access=0; %>

main.jsp:
<%@ include file="codesnippet.jsp"%>
<p>test:<%=access++; %>

@TagLib Directive:


### REQUEST:
* setAttribute
* getAttribute
* getCookies()
* getHeaderNames()
* getHeader(String name)
* getMethods()
* getParameter(String name)
* getQueryString(String name)
* get Locale()

### RESPONSE:
* response.setContentType("text/html");
* response.setHeader("Refresh",5);
* response.sendRedirect("success.jsp");
* response.addCookie(userCookie);

### refresh date:

<%response.setIntHeader("Refresh",3);
Date dd=new Date();
SimpleDateFormat sdf=new SimpleDateFormat("MM/dd/yyyy");
String date=sdf.format(dd);
%>

<p>test<%=date%></p>

-->out:
javax:
out.print
out.println
flush

### pageContext:
* setAttribute
* getAttribute
* findAttribute
* removeAttribute

### Session:
* setAttribute(String name,Object value)
* getAttribute(String name)
* removeAttribute(String name)

<%session.setAttribute("no",value)%>

## Application Object:
application.getAttribute(String name);

### Config:
* getInitParameter(String name)
* getInitParameterNames()
* getServletContext()
* getServletName()
