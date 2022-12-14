# Java Server Pages

## Introduction:

JSP is used to create web applications like the Servlet technology.
- It is kind of an extension to servlet.
- It is easier to maintain than a servlet.

## Advantages:

- Extension to servlet:
>> All the features of a servlet are available in JSP. In addition, we can use implicit objects, predefined tags and custom tags in JSP.

- Easy to maintain:
>> Separates our business and presentation logic.

- Faster deployment and development:
>> We don't need to recompile and redploy a JSP project again and again

- Less code than servlet:
>> We use custom tags in JSP, that significantly reduces the code.


## The lifecycle of JSP Page:
- Translation of JSP Page
- Compilation of JSP Page
- Classloading
- Instantiation
- Initialization
- Request Processing
- Destroy

## Scripting Elements:
The scripting elements provide the ability to insert java code inside the jsp. The three types of scripting elements are:
### JSP Scriptlet Tag:

In JSP, Java code can be written inside the jsp page using the scriptlet tag.
>> Syntax:
```jsp
<% "java source code" %>
```
### JSP Expression tag:
The code placed within this tag is written to the output stream of the response and is mainly used to print the values and methods of a program.
>> Syntax:
```jsp
<%= "statement" %>
```
### JSP Declaration Tag:

The JSP Declaration Tag is used to declare fields and methods. The code placed inside the declaration tag is placed outside the service() method of the autogenerated servlet.
>> Syntax:
```jsp
<%! field or method declaration %>
```

## JSP Scriptlet vs Declaration Tag

| Scriptlet Tag | Declaration Tag |
| --- | --- |
| Can only declare variables and not methods| Can Declare methods as well as variables|
| The declaration of the scriptlet tag is placed inside the _jspSerice() method | The declaration of the declaration tag is done outside the _jspService() method.|
