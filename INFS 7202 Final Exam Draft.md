# INFS 7202

The syntax of PHP native, PHP CodeIgniter

Good understanding of MVC, XML, JSON, AJAX. Coding Questions - format: fill in blank

Compulsory features

Front-end coding will not be assessed separately.

###### Structure

###### 40 multiple choice questions

###### 10 short answer or fill-in-blank questions

## Part 1

### Lecture 1

-   ##### Client-Side development

    -   Bootstrap
    -   HTML5
    -   Google Map
    -   Other JavaScript APIs
    -   JQuery

-   ##### ~~Deployment - will not be assessed~~  

    -   ~~How to buy a domain name~~
    -   ~~How to deploy your project to UQ Zone~~

-   ##### Should know how to create a form in HTML

-   ##### How to pass data from view to controller / from controller to view

### Lecture 2 introduction to WIS

-   ##### What is information

-   ##### What is a system

-   ##### What is an information system

-   ##### What are the key components of an information system 

-   ##### What is a Web Information System

    Web information system, or web-based information system, is an information system that uses Internet web technologies to deliver information and services, to users or other information systems / applications.

    A soft ware system whose main purpose is to publish ad maintain data by using hypertext-based principles.

-   ##### What are the two major types of Web Information Systems

    -   Informational
        -   Disseminate information(static or dynamic)
        -   Share information(among visitors or WISs)
    -   Transactional
        -   Conduct transactional business(B2C, C2C, B2B...)
        -   Perform tasks(simple, complex and collaborative)

-   ##### What are the major architectures of Web Information Systems



## Layers

-   ### Application

    -   FTP
    -   HTTP
    -   IMAP
    -   POP
    -   SMTP
    -   Telnet

-   ### Transport

    ###### Provides end-to-end communication services for applications

    ###### Manage the received data

    -   ##### TCP - Transmission Control Protocol

        -   A reliable connection-oriented transport service that provides end-to-end reliability, resequencing, and flow control.

    -   ##### UDP - User Datagram Protocol

        -   A connectionless("datagram") transport service  

-   ### Internet/Network

    -   IPv4
    -   IPv6

-   ### Data Link/Physical

    -   MAC



---



## Terminology

##### IP - Internet Protocol

##### HTTP - HyperText Transfer Protocol

HTTP is the protocol used to transfer Web Pages and files contained in web pages through the Internet at [application layer](#Application layer)

##### UDP - User Datagram Protocol

##### HTML - Hyper Text Markup Language

##### TCP - Transmission Control Protocol

##### FTP - File Transfer Protocol

Transfer files from one machine to another

##### SMTP - Simple Mail Transport Protocol

Email delivery

##### Telnet

Remote login

## Concepts

##### Protocols

Set of rules/agreements in telecommunications

##### Internet Protocol Suite(TCP/IP)

A family of communication protocols used to connect computer systems in a network

##### Application Layer

The TCP/IP architectural model has [four abstraction layers](#Layers)



---



## Security

#### Most Common Web Security Issues (or Web Application Attacks)

-   SQL injections, Broken authentication & session management, Insecure direct object references, Security misconfiguration, Cross-site request forgery (CSRF)
-   What they are and how to prevent

#### General Encryption algorithms

-   MD5 - Why no good
-   SALT - How it works
-   RSA - Calculation and application (e.g., digital signature)

#### Private Key System & Public Key System

![Screen Shot 2020-06-24 at 2.49.43 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-24 at 2.49.43 PM.png)

#### Encryption - Asymmetric Algorithm

##### ![Screen Shot 2020-06-24 at 2.50.26 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-24 at 2.50.26 PM.png)

#### RSA

Should know how to calculate

Generate the encryption key by using RSA algorithm

-   Encryption: $c = M^e$ mod n
    -   (e,n)
-   Decryption: $c = C^d$  mod n
    -   (d,n)





## Part 2 PHP and CodeIgniter

### PHP Syntax

-   #### Tags  

    -   PHP Scripts `<?php ?>`
    -   One-line comment `//`
    -   Make a comment block `/* */`

-   #### Variables

    -   Naming rules

    -   Built-in variables

        Super globals in PHP

        Always available in app scopes throughout a script

        -   `$GLOBALS`
        -   `$_SERVER`
        -   `$_GET`
        -   `$_POST`
        -   `$_FILES`
        -   `$_COOKIE`
        -   `$_SESSION`
        -   `$_REQUEST`
        -   `$_ENV`

    -   Variable operators

-   #### Function

    -   String functions - strcmp ...
        -   `print() ` outputs one or more strings, can return a true value
        -   `echo` same display to `print()`, but cannot return a value, considered as a father executed command.
        -   `printf()` outputs a formatted string; eg: `printf(%s, "hello");`
        -   `fprintf()` writes a formatted string to specified output stream(e.g., file or database)
    -   File functions - fopen

-   #### Operators  ![Screen Shot 2020-06-24 at 3.24.33 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-24 at 3.24.33 PM.png)

-   #### Create a form

    -   Solution 1

        ```php+HTML
        <form method = 'post' action = 'http://myapplicationcom/xxx.php/xx/xx'
        ```

    -   Solution 2

        ```php+HTML
        echo form_open('papers/login')
        ```

        -   Set base URL (e.g., project name) in your configuration preferences(config.php)

        -   This form points to your base URL plus the papers/login

        -   Why use echo?

            This function returns an HTML form opening tag as a string

### Cookie

##### cookies are stored in the user's computer

##### A cookie is often used to identify a user

-   ##### Q: What is cookie?

    A: a cookie is a small file that the server embeds on the user's computer. Each time the same computer requests a page with a browser, it will send to cookie as well. A cookie is often used to identify a user.

    ##### OR

    A: 

    1.  Created by the server
    2.  Stored on user's computer
    3.  Used to identify a user
    4.  Sent through with a page request

-   ##### How to create a cookie/retrieve a cookie/delete a cookie

-   ##### Understand all the parameters



### Sessions

-   ##### Q: what is session?

    **A:** 

    1.  A session is a way to store information (in variables) to be used across multiple pages.(Unlike a cookie, the information is not stored on the users computer.)
    2.  Session variables hod information about one single user, and are available to all pages in one application.
    3.  Session information is temporarily stored on server side and will be deleted after the user has left the website --- (you need to close the browser

-   A PHP session variable is used to store information about , or change settings for a user session.

-   Allow you to store user information on the server for later use (i.e. username, shopping items, etc)

-   Session variables hold information about one single user, and are available to all pages in one application

    -   Session information is **temporary** and will be deleted after the user has left the website.
    -   Need a permanent storage? Store the data in a database

-   ##### What are the differences between cookies and sessions? (4 marks)

    **A:**

    1.  Cookies are stored in the **user's hard disk**, but sessions are stored on the **server side**.
    2.  Cookies can keep information in the user's browser until deleted or expired while sessions are available as long as the browser maintains opened.
    3.  If you set the variable to "cookies", your user will not have to login in each time they enter your website; if you set the variable to "sessions", your users will have to login each time they re-open their browser.
    4.  Sessions are basically like tokens, which are generated at authentication.
    5.  Sessions are popularly used, as there is a chance of your cookies getting blocked if the user's browser security setting is set high.

-   How to start a session/store a session variable/free a session variable/destroy a session

-   Review the example in the next slide

-   Review the differences between destroy session and unset views in lecture demo 4



## XML

e**X**tensible **M**arkup **L**anguage

-   A markup language much like HTML

-   One of the most important technologies to support the WWW

-   What are the main differences between XML and HTML?

    A: 

    -   HTML is about displaying information, while XML is about describing information.
        -   HTML was designed to display data --- focus on how data looks.
        -   XML was design to transport and store data --- focus on what data is
    -   XML is not a replacement for HTML

#### Syntax

```xml
<course level='medium'>
    <Tutor> Jack </Tutor>
</course>
```

-   XML declaration
-   XML elements
    -   Element content 
    -   How to use symbol in element content
-   XML attributes
-   Naming rules

![Screen Shot 2020-06-24 at 6.58.41 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-24 at 6.58.41 PM.png)

## JSON

#### syntax

- Squiggles, Squares, Colons and Commas

  { } : Squiggly brackets act as 'containers'

  [ ] : Square brackets hold arrays

  :   : Names and values are separated by a colon

  ,  : array elements are separated by commas

#### JSON is like XML because:

- They are both 'self-describing' meaning that values are named, and thus 'human readable'
- Both are hierarchical. (i.e. you can have values within values)
- Both can be parsed and used by lots of programming languages
- Both can be parsed around using AJAX (i.e. XMLHttpRequest)

### JSON Object Creation in JS

![Screen Shot 2020-06-29 at 6.02.03 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-29 at 6.02.03 PM.png)

![Screen Shot 2020-06-29 at 6.02.48 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-29 at 6.02.48 PM.png)



## AJAX --- Asynchronous JavaScript And XML

- ##### AJAX is NOT a technology, but is a combination of existing technologies and a way of thinking

- ##### AJAX is the art of exchanging data with a server, and updates pmts of a web page, without reloading the whole page

  - AJAX allows web pages to be updated asynchronously by exchanging small amounts of data with the server behind the scenes



### How AJAX works?

![Screen Shot 2020-06-29 at 6.08.49 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-29 at 6.08.49 PM.png)

1. An event occurs in a Web page(e.g., the page is loaded, a button is clicked)
2. An **XMLHttpRequest object** is created by JavaScript
3. The XMLHttpRequest object sends a request to a web server
4. The server processes the request
5. The server sends a response back to the web page
6. The response is read by javaScript
7. Proper action(like page update) is performed by JavaScript





## Database

#### DBMS --- DataBase Management System

- A software that helps you to manage the records in a database

#### Relational DBMS

- A DBMS based on the relational data model
- Integrated collection of logically related data elements

#### 	SQL

- PHP + MySQL

- The Data Manipulation Language(DML)

- The Data Definition Language(DDL)

  | DML         |                                  |
  | ----------- | -------------------------------- |
  | SELECT      | Extracts data from a database    |
  | UPDATE      | Updates data in a database       |
  | DELETE      | Deletes data from a database     |
  | INSERT INTO | Inserts new data into a database |

  | DDL             |                              |
  | --------------- | ---------------------------- |
  | CREATE DATABASE | Creates a new database       |
  | ALTER DATABASE  | Modifies a database          |
  | CREATE TABLE    | Creates a new table          |
  | ALTER TABLE     | Modifies a table             |
  | DROP TABLE      | Deletes a table              |
  | CREATE INDEX    | Creates an index(search key) |
  | DROP INDEX      | Deletes an index             |

#### 	NoSQL --- Not only SQL

- A class of database management system(DBMS)
- Does not use SQL as querying language
- No fixed schema(formally described structure)
- No Joins (typical in databases operated with SQL)
- It's not a replacement for a RDBMS but compliments it
- Types of NoSQL Databases
  - ![Screen Shot 2020-06-29 at 6.46.58 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-29 at 6.46.58 PM.png)
  - Key-value store (Riak, Redis)
  - Document store (MongoDB, RavenDB)
  - Column-oriented database(e.g.: Cassandra, Hbase)
  - Graph database(e.g.: Neo4J, FlockDB)
  - DTD (concept, what for)



## IONIC

- #### How to create an Ionic project

  - Create an Ionic project with a tab bar using Ionic CLI (command-line interface) `ionic start demoapp tabs`
  - Run ionic serve within the app directory to see your app `ionic serve -l`
  - Create a new page `ionic generate page`

- #### Understand the basic UI element

  ##### Ionic component: <ion-list> <ion-item>

  List generally contains items with similar data content, such as images and text. It supports several interactions including swiping items to reveal options, dragging to recorder items within the list, and deleting items.

  ![Screen Shot 2020-06-29 at 6.59.49 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-29 at 6.59.49 PM.png)

  

## Flask (Concept)

A micro web framework

The "micro" in micro-framework aims to keep the core simple but extensible.

#### Advantages

- Many extensions in the Flask ecosystem
- Flask is used in projects big and small
- List of awesome-flask extensions and projects





