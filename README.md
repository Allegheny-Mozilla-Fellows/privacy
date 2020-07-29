##### Name:
Privacy, Ethics and Security.

##### GitHub link
git@github.com:Allegheny-Mozilla-Fellows/privacy.git


##### What is this?
This lab focuses on the importance of not only security but the ethics involved in hacking a database that could be used to exploit a person. The students will be taken through a tutorial that walks them through how SQL injection works, what it is, and how it can be used to harm someone. After the tutorial, the students are then asked numerous questions that tie back into the theme of privacy, security and ethics.

# Introduction

In this lab, we will explore the ethical implications that go along with hacking and databases. Lots of databases are out on the web that contain valuable information. What people don't know is that bypassing the security to access data from the database is a lot easier than one might think. For this lab, we will be looking at a website that mirrors what a banks website might look like that has a database connected to it that contains very valuable data. While there are many different techniques that someone may use to hack something, we will specifically be looking into SQL injection. SQL injection is an attack technique that exploits a security vulnerability occurring in the database layer of an application. Hackers use injections to obtain unauthorized access to the underlying data and structure of the system that they are trying to hack.

### How does a SQL injection attack occur?

SQL injection attacks occur when a web application does not validate values received from a web form, cookie, input parameter and more. There are several types of SQL injection but in this lab we are going to focus primarily on SQL injection through user input. Web applications typically accept user input through a form, and the front-end passes the user input to the back-end database for processing. If the web application fails to sanitize user input, an attacker can inject SQL statements of their choice into the back-end of the database basically allowing them to delete, copy, or modify the contents of the database.


### What does this look like?

Below is an example of of query statement being used to run the database on a web application.

``` SELECT * FROM customers WHERE customer_id ='12345' ```

This is simply a query telling the database to select everything from the customers table where the customer id = 12345.

Suppose someone wanted to inject a SQL statement into the query looking something like this.

``` SELECT * FROM customers WHERE customer_id='12345'; DELETE * FROM customers WHERE 'x' = 'x' ```.

This SQL injection statement is basically deleting everything that is in the customers table where there is a value being declared.



# Instructions

1. First, navigate to the cs.allegheny.edu website and boot up the web server. In order to do so, make sure you have python installed on your machine. You can check to see if you do by opening a terminal window and typing python --version. If you do not have python installed, you can simply go download python from their website https://www.python.org/downloads/ and download the version for your machine.


2. Once you have the server up and running and you can see the site, navigate through the site to get a feel for everything. You can see the site is acting like a bank with a home page, an about page, and a login page. Make sure to read through some of the material to get an idea of what this bank is trying to offer you.


3. After you have navigated through the bank's site and have an idea and an understanding of what it is the bank is trying to offer, the next step is the fun part. Let us try and hack this bank to see if we can extract any important data. Security is a very important measure when it comes to banking as it deals with very valuable information that could be harmful it used in an improper way.


4. As mentioned in the introduction, there are a few different types of methods you can use to hack a database. Just to be clear, we are trying to bypass the database associated with this site, so navigate to the page on the site where you think the hack can take place. This website offers lots of different types and techniques that will allow for this hack to happen https://www.wikihow.com/Hack-a-Database. Be sure to explore and play around with all of these different types of exploits.

5. After you have played around with the different types of exploits, lets try to bypass the forum and extract data from the database. Try typing in ` '` in the username box and press enter. Did you get an error? Now type in `"` and press enter. Did you get an error this time? If so, we have completed our first step to bypassing the login.

6. A big thing that is associated with databases is queries and the syntax of a query statement. Look back at the introduction document and specifically look at the example queries listed there. If the syntax is slightly off the database won't recognize it and this hack will not work. After you have done so, hit the back button on the web browser and go back to the login page.

7. There are a few common SQL injection statements. A big one is `or 1=1`. This statement simply makes everything always equal true. it doesn't matter what you put before this, `or 1=1` will always make the statement be true. Try putting this in along with `"` in the username box. Were you able to bypass the login with this SQL statement? If not we can try something else to bypass the login.

8. One more thing that is associated with SQL injection and SQL statements are inline comments. Usually you just add comments when you want to explain code but don't actually want that segment of code to run. For this particular query though, we need put a comment at the end of this statement in order for it to run. Trying putting  `#`, `/*`, `*/`, `--` at the end of the query statement to see if you can get your SQL injection query to work. Did one of them work? Did they all work. Make sure to answer the questions associated with this lab and keep in mind the ethical implications that go along with SQL injection and hacking.


### Leading questions
Students are also expected to answer the following questions based on what they have learned throughout this project.

1. Describe what is meant by ethical hacking in terms of database security and privacy?

2. What are some of the initial problems that allow for the database to be compromised?

3. How safe is the database when hosted by a website?

4. How safe do you think the data should be and why?

5. Describe your experience in hacking the database.

6. What was the leading flaw of the security to protect the database?

7.  What could be done to better protect the database in the future?

8. What data do you see in the database?

9. How could the data be exploited?

10. Describe the consequences of this exploitation.

11. Whose privacy is violated and how?

12. Who could be held liable for any damages caused by data abuse.

### Technical Questions

1. Where is Carrie Medina from?

2. What is Jesse Ortega’s eye color?

3. How old is Teresa Payne?

4. What is Jane Craig’s salary?

5. What is Katherine Jennings relationship status?

6. Who lives on Devrac circle?

7. What ethnicity is Sophie fletcher?

8. What state is James Walsh from?
